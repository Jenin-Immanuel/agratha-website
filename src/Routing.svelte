<script>
  import { meta, Route, router } from "tinro";

  import Home from "./pages/Home/Home.svelte";
  import Blog from "./pages/Blogs/Blog.svelte";
  import Events from "./pages/Events/Events.svelte";
  import Contact from "./pages/Home/components/Contactpage.svelte";

  import BlogsRouting from "./pages/Blogs/BlogsRouting.svelte";
</script>

<Route path="/">
  <Home />
</Route>
<Route path="/blog">
  <Blog />
</Route>
<!-- Blog Routes -->
<Route path="/blog/*">
  <BlogsRouting />
</Route>
<Route path="/events">
  <Events />
</Route>
<Route path="/contact">
  <Contact />
</Route>
