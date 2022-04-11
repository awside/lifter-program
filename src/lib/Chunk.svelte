<script lang="ts">
  import Block from './Block.svelte'
</script>

<div class="flex space-x-1 justify-center">
  <Block reps={5} type="warmup" status="standby" />
  <Block reps={5} type="warmup" status="ondeck" />
  <Block reps={5} type="warmup" status="miss" />
  <Block reps={3} type="warmup" status="good" />
  <Block reps={2} type="warmup" status="standby" />
  <Block reps={5} type="working" status="good" />
  <Block reps={5} type="working" status="standby" />
  <Block reps={5} type="working" status="ondeck" />
  <Block reps={5} type="working" status="miss" />
</div>
