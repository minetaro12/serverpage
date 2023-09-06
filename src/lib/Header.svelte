<script lang="ts">
  import { page } from "$app/stores";
</script>

<header>
  <h1>{$page.url.hostname.toUpperCase()}</h1>
</header>
