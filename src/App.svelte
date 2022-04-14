<script lang="ts">
  import Barbell from './lib/Barbell.svelte'
  import Header from './lib/Header.svelte'
  import Chunk from './lib/Chunk.svelte'
  import RepHandler from './lib/RepHandler.svelte'
  import NavBar from './lib/NavBar.svelte'
</script>

<main>
  <Header />
  <div class="container mx-auto max-w-lg space-y-5 py-5 px-5">
    <Barbell />
    <Chunk />
    <RepHandler />
  </div>
  <NavBar />
</main>
