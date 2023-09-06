<script lang="ts">
  import Header from "$lib/Header.svelte";
  import Footer from "$lib/Footer.svelte";

  // スタイルの読み込み
  import "@exampledev/new.css";
  import "../app.scss";
</script>

<svelte:head>
  <title>minetaro12 server</title>
  <link rel="icon" href="https://0sn.net/favicon.ico" />
</svelte:head>

<Header />
<slot />
<Footer />
