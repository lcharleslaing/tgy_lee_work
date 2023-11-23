<script>
  export let menuItems = [];
</script>

<!-- Implement your large screen menu structure here -->
<div class="navbar-center hidden lg:flex">
  <ul class="menu menu-horizontal px-1">
    {#each menuItems as menuItem}
      <li tabindex="0">
        <a>{menuItem.title}</a>
        {#if menuItem.submenu}
          <details>
            <summary>More</summary>
            <ul class="p-2">
              {#each menuItem.submenu as submenuItem}
                <li><a href={submenuItem.href}>{submenuItem.title}</a></li>
              {/each}
            </ul>
          </details>
        {/if}
      </li>
    {/each}
  </ul>
</div>
