<script lang="ts">
  import config from "../config";
  export let title: string | undefined = "";
  let outTitle: string;

  if (title) {
    outTitle = `${title} | ${config.title}`;
  } else {
    outTitle = config.title;
  }
</script>

<svelte:head>
  <title>{outTitle}</title>
  <link rel="icon" href="/favicon.ico" />
</svelte:head>
