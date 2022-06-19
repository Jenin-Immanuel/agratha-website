<script lang="ts">
  import Img1 from "../../../assets/cover/1.png";
  import Img2 from "../../../assets/cover/2.png";
  import Img3 from "../../../assets/cover/3.png";
  import Img4 from "../../../assets/cover/4.png";
  import Img5 from "../../../assets/cover/5.png";

  const Imgs = [Img1, Img2, Img3, Img4, Img5];
  const iteration = [0, 0];
</script>

<article>
  {#each iteration as i}
    <div>
      <ul>
        {#each Imgs as Img}
          <li><img src={Img} alt="" /></li>
        {/each}
      </ul>
    </div>
  {/each}
</article>

<style>
  img {
    display: block;
    width: 100%;
  }

  article {
    display: flex;
    width: 400vw;
    animation: bannermove 40s linear infinite;
  }

  div {
    width: 100%;
  }

  ul {
    display: flex;
    list-style-type: none;
    padding-left: 0;
    margin: 0;
    z-index: -9999;
  }

  li {
    width: 100%;
  }

  @keyframes bannermove {
    0% {
      transform: translateX(0);
    }

    100% {
      transform: translateX(-50%);
    }
  }

  @media (max-width: 768px) {
    article {
      width: 1200vw;
    }
  }
</style>
