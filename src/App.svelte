<script lang="ts">
  import Barbell from './lib/Barbell.svelte'
  import Header from './lib/Header.svelte'
  import Chunk from './lib/Chunk.svelte'
  import RepHandler from './lib/RepHandler.svelte'
  import Minus from './lib/svg/Minus.svelte'
  import LeftArrow from './lib/svg/LeftArrow.svelte'
</script>

<main>
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
  <Header />
  <div class="container mx-auto max-w-lg space-y-5 py-5 px-5">
    <Barbell />
    <Chunk />
    <RepHandler />
  </div>
</main>
