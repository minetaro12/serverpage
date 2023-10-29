<script lang="ts">
  import { page } from "$app/stores";
  import config from "../config";
</script>

<header>
  <h1>{$page.url.hostname.toUpperCase()}</h1>
  <nav>
    {#each config.nav as item}
      {#if $page.url.pathname === item.path}
        <span class="nav-item">{item.name}</span>
      {:else}
        <a href={item.path} class="nav-item">{item.name}</a>
      {/if}
    {/each}
  </nav>
</header>

<style lang="scss">
  .nav-item {
    margin-right: 10px;
  }
</style>
