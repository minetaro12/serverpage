<script lang="ts">
  import Head from "$lib/Head.svelte";
  import config from "../../config";
</script>

<Head title="Links" />

<h3>Links</h3>
<ul>
  {#each config.links as link}
    <li>
      {link.name}:
      <a href={link.path} target="_blank" rel="noopener noreferrer"
        >{link.linkName}</a
      >
    </li>
  {/each}
</ul>
