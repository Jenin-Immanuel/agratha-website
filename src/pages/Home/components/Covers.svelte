<script lang="ts">
  import { onMount } from 'svelte'
  import Img1 from "../../../assets/cover/1.png";
  import Button from "../../UIcomponents/Button.svelte";

  const Imgs = [
    {
      img: Img1,
      name: "Lorem Ipsum Dolor",
    },
    {
      img: Img1,
      name: "Lorem Ipsum Dolor",
    },
    {
      img: Img1,
      name: "Lorem Ipsum Dolor",
    },
  ];

  let width: Number;

  onMount(() => {
    width = window.innerWidth;
  })

  let styles = "padding: 1em 2em;"
</script>

<div class="outer">
  <h1>Covers</h1>
  <div class="container">
    {#each Imgs as Img}
      <div>
        <a href="http://www.google.com" target="_blank" tinro-ignore><img src={Img.img} alt="" /></a>
        <p>{Img.name}</p>
      </div>
    {/each}
  </div>
  <div class="button">
    {#if width < 786}
      <Button style={styles}>Watch More</Button>
    {:else}
      <Button>Watch More</Button>
    {/if}
  </div>
</div>

<style>
  .outer {
    text-align: start;
    padding-inline: 15vw;
  }

  .container, .button {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .container div p {
    text-align: center;
  }

  .button {
    margin-top: 1em;
  }

  img {
    max-width: 175px;
    max-height: 175px;
    border: 5px solid goldenrod;
    border-radius: 10px;
    transition: 0.1 transform ease-in-out;
  }

  img:hover {
    scale: 1.05;
  }

  @media (max-width: 768px) {
    h1 {
      font-size: 9vw;
    }

    p {
      font-size: 3.5vw;
    }
  }


  @media (min-width: 768px) {
    .container {
      flex-direction: row;
      gap: 2rem;
    }

    img {
      min-width: 225px;
      width: 100%;
      max-width: 300px;
      max-height: 300px;
    }
        
  }
  /* .outer {
    text-align: start;
    padding-inline: 15vw;
    padding-top: 4rem;
    margin-bottom: clamp(5rem, 10vw, 15rem);
  }

  .container {
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: flex-start;
    margin-bottom: 2em;
  }

  .container > div {
    display: flex;
    flex-direction: column;
  }

  .button {
    display: flex;
    justify-content: center;
    margin-top: 4em;
  }

  img {
    max-width: 20em;
    border-radius: 10px;
    max-height: 17em;
    margin-right: 6em;
    cursor: pointer;
    border: 10px solid #ffd700;
    transition: all 0.3s ease-in-out;
  }

  img:hover {
    transform: scale(1.1);
  }

  @media (max-width: 768px) {
    .outer {
      width: 100vw;
    }
    .container {
      flex-direction: column;
      align-items: flex-start;
      justify-content: flex-start;
    }

    img {
      transform: scale(0.7);
      margin: 0;
    }

    h1 {
      font-size: 9vw;
    }

    p {
      text-align: center;
      font-size: 6vw;
    }
  } */
</style>
