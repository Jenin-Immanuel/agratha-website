<script lang="ts">
  import insta from "../../../assets/icons/insta.png";
  import facebook from "../../../assets/icons/fb.png";
  import youtube from "../../../assets/icons/yt.png";
  import { each } from "svelte/internal";

  const Medias = [
    {
      img: insta,
      name: "Instagram",
      link: "https://www.instagram.com/band_agratha/",
    },
    {
      img: facebook,
      name: "Facebook",
      link: "https://m.facebook.com/musicclubofkct/posts",
    },
    {
      img: youtube,
      name: "Youtube",
      link: "https://www.youtube.com/channel/UCsY82qu1fCUVEt8iE4dmLPw",
    },
  ];
</script>

<div>
  <h1>Follow Us</h1>
  <p>
    Follow our instagram to page to get instant updates about the club. Follow
    our facebook and youtube, as we post our cover versions and events songs
  </p>
  <section>
    {#each Medias as media}
      <a href={media.link} target="_blank">
        <img src={media.img} alt="" />
      </a>
    {/each}
  </section>
</div>

<style>
  div {
    padding-inline: 15vw;
    text-align: start;
    padding-top: 4rem;
    margin-bottom: clamp(5rem, 10vw, 15rem);
  }

  section {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: 5em;
    margin-block: 3rem;
  }

  section a img {
    max-height: 10vh;
    max-width: 10vw;
    display: flex;
    justify-content: center;
  }

  @media (max-width: 768px) {
    h1 {
      font-size: 9vw;
    }

    p {
      font-size: 4vw;
    }
  }
</style>
