<script lang="ts"></script>

<div>
  <h2>We The</h2>
  <h1>Band Agratha</h1>
</div>

<style>
  div {
    padding: 5rem;
  }

  h2 {
    font-size: 4vw;
    letter-spacing: 2px;
  }

  h1 {
    height: 20vw;
    font-family: "Dancing Script", cursive;
    font-size: 9vw;
    line-height: 1;
    text-align: center;
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

  @media (max-width: 768px) {
    h1 {
      font-size: 9.5vw;
    }
  }
</style>
