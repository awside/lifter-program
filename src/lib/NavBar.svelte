<script lang="ts">
  import LeftArrow from './svg/LeftArrow.svelte'
  import Minus from './svg/Minus.svelte'
</script>

<div
  class="fixed bottom-0 flex h-20 w-full justify-center border-t-2 border-black bg-slate-300"
>
  <div class="flex items-center justify-around space-x-5">
    <div class="rounded-md border-4 border-blue-500 bg-white p-2 px-4">
      <Minus />
    </div>
    <div class="rounded-md border-4 border-blue-500 bg-white p-2 px-4">
      <LeftArrow />
    </div>
    <div class="rounded-md border-4 border-blue-500 bg-white p-2 px-4">
      <Minus />
    </div>
    <div class="rounded-md border-4 border-blue-500 bg-white p-2 px-4">
      <LeftArrow />
    </div>
  </div>
</div>
