<script lang="ts">
  import { meta } from "tinro";
  const route = meta();
</script>

<div class="outer-box">
  <slot />
  {#if $route.url.length > 6}
    <a href="/blog" class="button"><p>Return to blog page</p></a>
  {/if}
</div>

<style>
  .outer-box {
    padding-inline: 15vw;
    padding-top: 7.5rem;
    text-align: start;
  }
  .button {
    text-decoration: none;
    color: inherit;
  }

  .button > p {
    text-align: end;
    font-size: 0.75em;
    color: grey;
  }
  div {
    padding-inline: 15vw;
    padding-top: 10rem;
  }

  @media (max-width: 768px) {
    .outer-box {
      padding-inline: 0;
    }
  }
</style>
