<script lang="ts">
  import type { Writable } from 'svelte/store'
  import type { tExercise } from './toolbox'

  export let exercise: tExercise
  export let state: Writable<string>
</script>

<div class="flex h-10 border-2 border-black">
  <div
    class="flex flex-1 items-center justify-center bg-slate-200 text-xl font-bold uppercase"
  >
    {exercise}
  </div>
  <div
    bind:textContent={$state}
    contenteditable="true"
    class="flex flex-1 cursor-pointer items-center text-2xl justify-center outline-none"
  >
    {$state}
  </div>
</div>
