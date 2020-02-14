<script>
  import SquareGrid from "./SquareGrid.svelte";

  let size = 10;
</script>

<h1>Dan's sveltey supersquare</h1>

<p>{size}</p>
<input type="range" min={0} bind:value={size} />

<SquareGrid {size} />
