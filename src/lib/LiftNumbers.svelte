<script lang="ts">
  import InputBox from './InputBox.svelte'
  import { benchpress, deadlift, powerclean, press, squat } from '../lib/store'
</script>

<div>
  <InputBox exercise="squat" state={squat} />
  <InputBox exercise="press" state={press} />
  <InputBox exercise="benchpress" state={benchpress} />
  <InputBox exercise="deadlift" state={deadlift} />
  <InputBox exercise="powerclean" state={powerclean} />
</div>
