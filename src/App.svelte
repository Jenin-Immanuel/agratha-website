<script lang="ts">
  import Home from "./pages/Home/Home.svelte";

  window.onbeforeunload = () => {
    window.scrollTo(0, 0);
  };
</script>

<main>
  <Home />
</main>

<style>
  @import url("https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Lato&display=swap");
  /* @import url("https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&display=swap"); */

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
    background-color: #333;
    color: #fff;
  }

  :global(p) {
    font-size: 2vw;
  }

  :global(h1) {
    font-family: "Dancing Script", cursive;
    font-size: 5vw;
    background: linear-gradient(
      90deg,
      rgba(186, 148, 62, 1) 0%,
      rgba(236, 172, 32, 1) 20%,
      rgba(186, 148, 62, 1) 39%,
      rgba(249, 244, 180, 1) 50%,
      rgba(186, 148, 62, 1) 60%,
      rgba(236, 172, 32, 1) 80%,
      rgba(186, 148, 62, 1) 100%
    );
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    animation: shine 4s infinite;
    background-size: 200%;
    background-position: left;
  }

  @keyframes shine {
    to {
      background-position: right;
    }
  }

  main {
    text-align: center;
  }

  @media (max-width: 768px) {
    :global(h1) {
      font-size: 4rem;
    }
    :global(p) {
      font-size: 1.2rem;
    }
  }
</style>
