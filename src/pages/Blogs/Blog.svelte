<script lang="ts">
  // import { onMount } from "svelte";
  // let blogs: any = [];
  // let url = "./src/pages/Blogs/blogs.json";
  // onMount(async () => {
  //   const res = await fetch(url);
  //   const data = await res.json();
  //   blogs = data;
  // });
  // fetch("./src/pages/Blogs/blogs.json")
  //   .then((res) => res.json())
  //   .then((json) => (blogs = json))
  //   .catch((err) => console.error(err));
  // console.log(blogs);
  const oldblogs = [
    {
      id: "1000",
      title: "Music Theory in 10 min",
      author: "Akash Shann",
      date: "2022-06-25",
    },
    {
      id: "1001",
      title: "Another blog",
      author: "Akash Loganathan",
      date: "2022-06-25",
    },
  ];
  // console.log(oldblogs);
</script>

<div class="outer-box">
  <h1>Agratha Blogs</h1>

  <section>
    {#each oldblogs as blog}
      <a href="/blog/{blog.id}">
        <div>
          <h2 class="title">{blog.title}</h2>
          <h6 class="author">{blog.author}</h6>
          <h6 class="date">Publilshed on: {blog.date}</h6>
        </div>
      </a>
    {/each}
  </section>
</div>

<style>
  .outer-box {
    padding-inline: 15vw;
    padding-top: 7.5rem;
    text-align: start;
  }

  section {
    margin-top: 5em;
  }
  section > a > div {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, 1fr);
    cursor: pointer;
    padding: 1em 2em;
    border-radius: 20px;
    transform: scale(0.9);
    box-shadow: 10px 10px 8px #000;
    margin-bottom: 2em;
    transition: 0.4s ease-in-out;
  }

  a {
    text-decoration: none;
    color: inherit;
  }
  section > a > div:hover {
    transform: scale(0.85);
  }

  section .date {
    text-align: end;
  }

  h2,
  h6 {
    margin: 0;
    padding: none;
  }

  h2 {
    font-size: 2em;
  }

  h6 {
    font-size: 1em;
  }

  .title {
    grid-area: 1 / 1 / 2 / 4;

    background: linear-gradient(
      90deg,
      rgba(186, 148, 62, 1) 0%,
      rgba(236, 172, 32, 1) 20%,
      rgba(186, 148, 62, 1) 39%,
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

  .author {
    grid-area: 3 / 1 / 4 / 2;
  }

  .date {
    grid-area: 2 / 3 / 3 / 4;
  }

  @media (max-width: 768px) {
    .outer-box {
      padding-inline: 0;
    }

    h1 {
      font-size: 9.5vw;
      text-align: center;
    }

    section {
      display: flex;
      flex-direction: column;
      gap: 3em;
    }

    section > a > div {
      display: flex;
      flex-direction: column;
      padding: 0;
      gap: 0.5em;
      box-shadow: none;
    }

    h2 {
      font-size: 1.5em;
    }

    h6 {
      font-size: 0.75em;
      font-weight: normal;
    }
  }
</style>
