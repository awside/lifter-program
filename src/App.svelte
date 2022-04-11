<script lang="ts">
  import Barbell from './lib/Barbell.svelte'
  import Header from './lib/Header.svelte'
  import LiftNumbers from './lib/LiftNumbers.svelte'
  import Path from './lib/Path.svelte'
  import Chunk from './lib/Chunk.svelte'
</script>

<main>
  <Header />
  <div class="container mx-auto max-w-lg space-y-5 py-5 px-5">
    <Barbell />
    <Chunk />
    <Path />
    <LiftNumbers />
  </div>
</main>
