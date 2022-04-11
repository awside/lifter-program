<script lang="ts">
  import plateCalculator from 'plate-calculator'
  import Plate from './Plate.svelte'
  import { squat } from './store'
  import type { tWeight, tWidth } from './toolbox'

  let weight: number
  let plates: { plate: tWeight }[]
  let width: tWidth

  $: {
    width = weight >= 700 ? 'skinny' : 'normal'
    plates = getPlates(weight)
    console.log(plates)
  }

  squat.subscribe((v) => {
    weight = +v
  })

  function getPlates(total: number): { plate: tWeight }[] {
    let a: tWeight[] = []
    let calc = plateCalculator.calculate(total, {
      set: [45, 25, 10, 5, 2.5, 1.25, 1, 0.75, 0.5, 0.25],
    })

    calc.plates.forEach((e: { plateWeight: number; qty: 4 }) => {
      ;[...Array(e.qty / 2)].forEach(() => {
        a.push(e.plateWeight.toString().replace('0.', '.') as tWeight)
      })
    })

    return a.map((e) => {
      return { plate: e }
    })
  }
</script>

<div
  class="flex h-56 flex-row items-center overflow-hidden border-2 border-black bg-blue-300"
>
  <Plate weight="bar" {width} />
  {#each plates as plate (plate)}
    <Plate weight={plate.plate} {width} />
  {/each}
</div>
