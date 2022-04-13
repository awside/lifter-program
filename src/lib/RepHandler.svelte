<script lang="ts">
  import Button from './Button.svelte'
  import LeftArrow from './svg/LeftArrow.svelte'
  import Minus from './svg/Minus.svelte'
  import Plus from './svg/Plus.svelte'
  import RightArrow from './svg/RightArrow.svelte'

  let isEditReps = false
  let buttonName = 'EDIT REPS'

  $: buttonName = isEditReps ? 'DONE' : 'EDIT REPS'

  function toggleEditReps() {
    isEditReps = !isEditReps
  }
</script>

<div class="flex items-center justify-around">
  <div class="rounded-md border-4 border-blue-500 bg-white p-2 px-4">
    {#if isEditReps == true}
      <Minus />
    {:else}
      <LeftArrow />
    {/if}
  </div>
  <div class="flex-1">
    <Button name={buttonName} action={toggleEditReps} />
  </div>
  <div class="rounded-md border-4 border-blue-500 bg-white p-2 px-4">
    {#if isEditReps == true}
      <Plus />
    {:else}
      <RightArrow />
    {/if}
  </div>
</div>
