<script lang="ts">
  import Barbell from './lib/Barbell.svelte'
  import Header from './lib/Header.svelte'
  import Chunk from './lib/Chunk.svelte'
  import RepHandler from './lib/RepHandler.svelte'
  import NavBar from './lib/NavBar.svelte'
</script>

<main>
  <Header />
  <div class="container mx-auto max-w-md space-y-5 px-5 pb-24">
    <div class="h-10" />
    <Chunk />
    <Barbell />
    <RepHandler />
  </div>
  <NavBar />
</main>
