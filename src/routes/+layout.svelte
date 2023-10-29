<script lang="ts">
  import Head from "$lib/Head.svelte";
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";

  export let data;

  // スタイルの読み込み
  import "@exampledev/new.css";
  import "@xz/fonts/serve/inter.css";

  import { fly } from "svelte/transition";
</script>

<!-- タイトルのリフレッシュ -->
{#key data.pathname}
  <Head />
{/key}

<div id="wrapper">
  <Header />
  {#key data.pathname}
    <main in:fly={{ delay: 200, x: 200 }} out:fly={{ duration: 200, x: -200 }}>
      <slot />
    </main>
  {/key}
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
