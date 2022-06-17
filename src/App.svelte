<script lang="ts">
  import Home from "./pages/Home/Home.svelte";

  window.onbeforeunload = function () {
    window.scrollTo(0, 0);
  };
</script>

<main>
  <Home />
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Lato&display=swap");

  :root {
    font-family: "Lato", sans-serif;
  }

  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }

  :global(body) {
    margin: 0 auto;
    overflow-x: hidden;
  }

  main {
    text-align: center;
  }
</style>
