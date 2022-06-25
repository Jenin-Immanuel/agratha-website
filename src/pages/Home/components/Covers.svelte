<script lang="ts">
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

  //   const Imgs = [Img1, Img1, Img1];
</script>

<div class="outer">
  <h1>Covers</h1>
  <div class="container">
    {#each Imgs as Img}
      <div>
        <img src={Img.img} alt="" />
        <p>{Img.name}</p>
      </div>
    {/each}
  </div>
  <div class="button">
    <Button>Watch More</Button>
  </div>
</div>

<style>
  .outer {
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
  }
</style>
