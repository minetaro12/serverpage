<script lang="ts">
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";

  // スタイルの読み込み
  import "@exampledev/new.css";
  import "@xz/fonts/serve/inter.css";
</script>

<div id="wrapper">
  <Header />
  <main>
    <slot />
  </main>
  <Footer />
</div>

<style lang="scss">
  :global(body) {
    height: 100svh;
    box-sizing: border-box;
  }

  #wrapper {
    display: flex;
    flex-direction: column;
    height: 100%;

    main {
      flex: 1;
    }
  }
</style>
