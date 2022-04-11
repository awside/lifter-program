<script lang="ts">
  export let type: 'warmup' | 'working'
  export let status: 'standby' | 'ondeck' | 'miss' | 'good'
  export let reps: number = 1
</script>

<div
  class="flex h-8 w-8 items-center justify-center border-4 border-black bg-green-400 font-bold"
>
  {reps}
</div>
