<script lang="ts">
</script>

<div>
  <slot />
  <a href="/blog" class="button"><p>Return to blog page</p></a>
</div>

<style>
  .button {
    text-decoration: none;
    color: inherit;
  }

  .button > p {
    text-align: end;
    font-size: 1.5em;
  }
  div {
    padding-inline: 15vw;
    padding-top: 10rem;
  }
</style>
