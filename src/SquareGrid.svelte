<script>
  import Square from "./Square.svelte";
  export let size;

  $: enumerator = new Array(size);
</script>

<style>
  div.grid {
    display: flex;
    flex-direction: column;
  }

  div.row {
    display: flex;
    flex-direction: row;
  }
</style>

<p>Number of squares: {size * size}</p>

<div class="grid">
  {#each enumerator as _, x}
    <div class="row">
      {#each enumerator as _, y}
        <Square {x} {y}>x:{x} y:{y}</Square>
      {/each}
    </div>
  {/each}
</div>
