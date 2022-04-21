<script lang="ts">
  import Block from './Block.svelte'
</script>

<div class="flex items-center justify-center space-x-1">
  <Block reps={5} status="good" />
  <Block reps={5} status="miss" />
  <Block reps={5} status="ondeck" />
  <Block reps={3} status="standby" />
  <Block reps={2} status="standby" />
  <div class="h-1 w-2 bg-black" />
  <Block reps={5} status="ondeck" />
  <Block reps={5} status="good" />
  <Block reps={5} status="standby" />
</div>
