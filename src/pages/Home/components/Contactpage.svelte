<script lang="ts">
  import Button from "../../UIcomponents/button.svelte";

  function submit() {
    alert(
      "Thank you for your message!\nWe will get back to you as soon as possible."
    );
  }
  const buttonStyle =
    "grid-area: 3 / 2 / 4 / 4; padding: 0.75em 4em; font-size: 2em;";

  //TODO: Add mailing facilities to this form
</script>

<div>
  <h1>Contact US</h1>

  <form on:submit|preventDefault>
    <input type="text" placeholder="Your Name" id="name" required />
    <input type="email" placeholder="Your Email Address" id="email" required />
    <textarea
      name="Message"
      placeholder="Your Message"
      id=""
      cols="30"
      rows="20"
      required
    />
    <Button on:click={submit} style={buttonStyle}>Submit</Button>
  </form>
</div>

<style>
  div {
    padding-inline: 15vw;
    text-align: start;
    padding-top: 6rem;
    /* margin-bottom: clamp(5rem, 10vw, 15rem); */
  }

  div form {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: 0.5fr 2fr 0.5fr;
    grid-gap: 3em;
    margin-top: 3em;
  }
  div form #name {
    grid-area: 1 / 1 / 2 / 3;
  }
  div form #email {
    grid-area: 1 / 3 / 2 / 5;
  }
  div form textarea {
    grid-area: 2 / 1 / 3 / 5;
  }

  input,
  textarea {
    background: none;
    outline: none;
    border: 1px solid red;
    border-radius: 50px;
    padding: 2em 2em;
    font-size: 1em;
    color: white;
    --color-bg: #333;
    background: linear-gradient(90deg, var(--color-bg), var(--color-bg))
        padding-box,
      linear-gradient(
          90deg,
          rgba(186, 148, 62, 1) 0%,
          rgba(236, 172, 32, 1) 20%,
          rgba(186, 148, 62, 1) 39%,
          rgba(249, 244, 180, 1) 50%,
          rgba(186, 148, 62, 1) 60%,
          rgba(236, 172, 32, 1) 80%,
          rgba(186, 148, 62, 1) 100%
        )
        border-box;
    border: 4px solid transparent;
  }
  textarea {
    padding: 2em 3em;
  }

  @media (max-width: 768px) {
    div {
      display: none;
    }
  }
</style>
