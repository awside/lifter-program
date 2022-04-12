<script lang="ts">
  import Button from './Button.svelte'
  import LeftArrow from './svg/LeftArrow.svelte'
  import Minus from './svg/Minus.svelte'
  import Plus from './svg/Plus.svelte'
  import RightArrow from './svg/RightArrow.svelte'
</script>

<div class="flex items-center justify-around">
  <div class="rounded-md border-2 border-blue-500 bg-white p-2">
    <Minus />
  </div>
  <Button name="EDIT REPS" />
  <div class="rounded-md border-2 border-blue-500 bg-white p-2">
    <Plus />
  </div>
</div>
