<script lang="ts">
  let open = false;
</script>

<nav>
  <ul class:open>
    <li><a href="#0">About</a></li>
    <li><a href="#0">Blog</a></li>
    <li><a href="#0">Events</a></li>
    <li><a href="#0">Contact</a></li>
  </ul>
  <div class="hamburger" class:open on:click={() => (open = !open)}>
    <span class="bar" />
    <span class="bar" />
    <span class="bar" />
  </div>
</nav>

<style>
  li {
    list-style: none;
  }

  a {
    text-decoration: none;
  }

  nav {
    display: flex;
    justify-content: space-between;
    width: 100vw;
    position: absolute;
    align-items: center;
    padding: 1rem 1.5rem;
    background-color: rgba(255, 255, 255, 0.5);
    backdrop-filter: blur(10px);
    z-index: 99999;
  }

  .hamburger {
    display: none;
  }

  .bar {
    display: block;
    width: 25px;
    height: 3px;
    margin: 5px auto;
    -webkit-transition: all 0.3s ease-in-out;
    transition: all 0.3s ease-in-out;
    background-color: #333;
  }

  ul {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  li {
    margin-left: 5rem;
  }

  a {
    font-size: 1.6rem;
    font-weight: 400;
    color: #333;
  }

  a::hover {
    color: #482ff7;
  }

  @media only screen and (max-width: 768px) {
    ul {
      position: fixed;
      left: -150%;
      top: 3rem;
      flex-direction: column;
      background-color: rgba(255, 255, 255, 0.6);
      backdrop-filter: blur(10px);
      width: 100vw;
      border-radius: 10px;
      text-align: center;
      transition: 0.3s;
      box-shadow: 0 10px 27px rgba(0, 0, 0, 0.05);
      z-index: 9999;
    }

    ul.open {
      left: -5%;
    }

    li {
      margin: 2.5rem 0;
    }

    .hamburger {
      display: block;
      cursor: pointer;
    }

    .hamburger.open .bar:nth-child(2) {
      opacity: 0;
    }

    .hamburger.open .bar:nth-child(1) {
      transform: translateY(8px) rotate(45deg);
    }

    .hamburger.open .bar:nth-child(3) {
      transform: translateY(-8px) rotate(-45deg);
    }
  }
</style>
