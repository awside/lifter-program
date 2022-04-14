<script lang="ts">
  export let name: string
  export let action: () => void = () => {}
</script>

<div
  on:click={action}
  class="flex h-10 cursor-pointer select-none items-center rounded-md border-2 border-blue-500 px-2 text-blue-500"
>
  {name}
</div>
