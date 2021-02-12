<script>
  import { onMount } from "svelte";
  export let date;

  onMount(async () => {
    const res = await fetch("/api/date");
    const newDate = await res.text();
    date = newDate;
  });
</script>

<svelte:head>
  <title>devisa.io</title>
</svelte:head>

<style>
  h1 {
    font-size: 5.9rem;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    font-weight: 100;
    /* text-shadow: 1px 2px 9px rgba(0,0,0,0.4); */
    /* color: #fff; */
  }
  :global(body) {
    /* background-image: linear-gradient(#343048, #291f32); */
    max-height: 100%;
    max-width: 100%;
    overflow: auto;
  }
  div {
    display: block;
    position: absolute;
  }
  #i {
    background: #291f32;
    color: #b0fe76;
  }

</style>

<main>
  <h1>welcome to <span style="background: #b0fe76; color: #444054">devisa</span></h1>
</main>
