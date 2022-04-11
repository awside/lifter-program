<script lang="ts">
  import type { tWeight, tWidth } from './toolbox'

  export let weight: tWeight
  export let width: tWidth = 'normal'

  let attr: {
    base: string
    width: string
    border: string
    textSize: string
    verticalText: string
    weight: string
    getTailwind: () => string
  } = {
    base: 'flex items-center justify-center rounded-md border-slate-800 font-semibold',
    width: width == 'normal' ? ' w-8' : ' w-5',
    border: width == 'normal' ? ' border-4' : ' border-2',
    textSize: width == 'normal' ? ' text-lg' : ' text-md',
    verticalText: 'writing-mode:vertical-rl',
    weight: weight,
    getTailwind: () => {
      return attr.base + attr.width + attr.border + attr.textSize
    },
  }

  switch (weight) {
    case 'bar':
      attr.base += ' bg-black'
      attr.base += ' h-10'
      attr.base += ' text-white'
      attr.width = ' w-12'
      attr.base = attr.base.replace(' rounded-md', '')
      attr.verticalText = ''
      attr.weight = '45'
      break
    case '45':
      attr.base += ' bg-red-500'
      attr.base += ' h-48'
      break
    case '25':
      attr.base += ' bg-green-500'
      attr.base += ' h-36'
      break
    case '10':
      attr.base += ' bg-blue-500'
      attr.base += ' h-28'
      break
    case '5':
      attr.base += ' bg-amber-500'
      attr.base += ' h-20'
      break
    case '2.5':
      attr.base += ' bg-white'
      attr.base += ' h-16'
      break
    case '1.25':
      attr.base += ' bg-fuchsia-500'
      attr.base += ' h-12'
      break
    case '1':
      attr.base += ' bg-emerald-500'
      attr.base += ' h-12'
      break
    case '.75':
      attr.base += ' bg-cyan-500'
      attr.base += ' h-12'
      break
    case '.5':
      attr.base += ' bg-rose-500'
      attr.base += ' h-12'
      break
    case '.25':
      attr.base += ' bg-yellow-500'
      attr.base += ' h-12'
      break
  }
</script>

<div class={attr.getTailwind()} style={attr.verticalText}>
  {attr.weight}
</div>
