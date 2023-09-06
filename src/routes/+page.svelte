<script lang="ts">
  import config from "../config";
</script>

<h3>Links</h3>
<ul>
  {#each config.links as link}
    <li>
      {link.name}: <a href={link.path} target="_blank" rel="noopener noreferrer">{link.linkName}</a>
    </li>
  {/each}
</ul>
