<script>
  export let menuItems = [];
</script>

<ul class="menu">
  {#each menuItems as menuItem}
    <li>
      <a href={menuItem.href}>{menuItem.title}</a>
      {#if menuItem.submenu}
        <ul class="p-2">
          {#each menuItem.submenu as submenuItem}
            <li><a href={submenuItem.href}>{submenuItem.title}</a></li>
          {/each}
        </ul>
      {/if}
    </li>
  {/each}
</ul>
