<script context="module">
  export function preload() {
    return this.fetch(`blog.json`)
      .then((r) => r.json())
      .then((posts) => {
        return { posts };
      });
  }
</script>

<script>
  import Post from "../components/Post.svelte";
  export let posts;
</script>

<style>
  .Posts {
    display: grid;
    grid-template-columns: 1fr;
    justify-content: space-between;
    gap: 15px;
  }
</style>

<svelte:head>
  <title>Filosofía y Café</title>
</svelte:head>

<div class="Home">
  <div class="Posts">
    {#each posts as post}
      <Post {post} />
    {/each}
  </div>
</div>
