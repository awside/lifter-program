<script lang="ts">
  export let status: 'standby' | 'ondeck' | 'miss' | 'good'
  export let reps: number = 1

  const styles = {
    standby: ' border-slate-500',
    ondeck: ' border-black',
    miss: ' border-black bg-red-400',
    good: ' border-black bg-green-400',
  }

  let ondeck = status == 'ondeck' ? ' border-black' : ' border-slate-200'
  let style = styles[status]
</script>

<div class={'border-t-4 border-b-4 py-1' + ondeck}>
  <div
    class={'flex h-9 w-9 items-center justify-center rounded-md border-4 text-2xl font-bold' +
      style}
  >
    {reps}
  </div>
</div>
