<script lang="ts">
  import { meta, Route, router } from "tinro";

  import BlogTemplate from "./BlogTemplate.svelte";

  // Importing the blogs
  import Blog1000 from "./1000.svx";
  import Blog1001 from "./1001.svx";
</script>

<BlogTemplate>
  <Route path="/1000"><Blog1000 /></Route>
  <Route path="/1001"><Blog1001 /></Route>
</BlogTemplate>

<style></style>
