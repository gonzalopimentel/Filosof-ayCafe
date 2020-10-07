<script>
  import Header from "../components/Header.svelte";
  import Nav from "../components/Nav.svelte";
  import Main from "../components/Main.svelte";
  import Footer from "../components/Footer.svelte";
  export let segment;
</script>

<style>
</style>

<Header />
<Nav {segment} />

<Main>
  <slot />
</Main>
<Footer />
