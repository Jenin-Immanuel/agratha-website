<script lang="ts">
  import { createEventDispatcher } from "svelte";

  let styles = $$props.style;

  const dispatch = createEventDispatcher();
  const click = () => dispatch("click");
</script>

<button on:click={click} style={styles}>
  <slot />
</button>

<style>
  button {
    font-size: 1em;
    position: relative;
    padding: 1em;
    box-sizing: border-box;
    cursor: pointer;
    background: none;
    border: none;
  }

  button {
    background-image: linear-gradient(
      to right,
      #f09819 0%,
      #edde5d 51%,
      #f09819 100%
    );
    padding: 1em 3.5em;
    text-align: center;
    letter-spacing: 1px;
    /* text-transform: uppercase; */
    transition: 0.5s;
    background-size: 200% auto;
    color: white;
    border-radius: 50px;
    display: block;
  }

  button:hover {
    background-position: right center;
    color: #fff;
    text-decoration: none;
    transform: scale(1.1);
  }
</style>
