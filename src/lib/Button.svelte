<script lang="ts">
  export let name: string

  const handleClick = () => {
    console.log(name)
  }
</script>

<div
  on:click={handleClick}
  class="border-2 border-blue-500 px-2 py-1 rounded-md text-blue-500 text-sm"
>
  {name}
</div>
