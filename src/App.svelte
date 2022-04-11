<script lang="ts">
  import Barbell from './lib/Barbell.svelte'
  import Header from './lib/Header.svelte'
  import LiftNumbers from './lib/LiftNumbers.svelte'
</script>

<main>
  <Header />
  <div class="container max-w-lg mx-auto space-y-5 py-5 px-5">
    <Barbell />
    <LiftNumbers />
  </div>
</main>
