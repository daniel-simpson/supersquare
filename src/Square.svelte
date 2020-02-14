<script>
  import { fade } from "svelte/transition";

  export let x;
  export let y;

  $: isEven = (x + y) % 2 === 0;
</script>

<style>
  div {
    min-width: 50px;
    height: 50px;
    display: flex;
    align-items: center;
    justify-items: center;
    border: 1px solid black;
  }

  .even {
    background-color: rgba(100, 100, 100, 0.5);
  }

  p {
    display: block;
    margin: 0 auto;
    text-align: center;
  }
</style>

<div transition:fade={{ duration: 100 }} class:even={isEven}>
  <p>{y + 1}</p>
</div>
