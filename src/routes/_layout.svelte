<script>
  import Header from "../components/Header.svelte";
  import Nav from "../components/Nav.svelte";
  import Main from "../components/Main.svelte";
  export let segment;
</script>

<style>
</style>

<Header />
<Nav {segment} />

<Main>
  <slot />
</Main>
