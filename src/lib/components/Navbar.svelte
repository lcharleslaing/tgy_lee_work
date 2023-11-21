<script>
  import MenuLinks from "./MenuLinks.svelte";

  const menuItems = [
    { title: "Home", href: "/" },
    {
      title: "Auth",
      href: "/",
      submenu: [
        { title: "Register", href: "/" },
        { title: "Signin", href: "/" },
        { title: "Login", href: "/" },
      ],
    },
    {
      title: "Lee's Time",
      href: "/",
      submenu: [
        { title: "Physical Work", href: "/" },
        { title: "Brain Work", href: "/" },
        { title: "Rates", href: "/" },
        { title: "Categories", href: "/" },
      ],
    },
    { title: "Reports", href: "/" },
  ];
</script>

<div class="navbar bg-base-100 shadow">
  <div class="navbar-start">
    <div class="dropdown">
      <!-- svelte-ignore a11y-no-noninteractive-tabindex -->
      <!-- svelte-ignore a11y-label-has-associated-control -->
      <label tabindex="0" class="btn btn-ghost lg:hidden">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-5 w-5"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h8m-8 6h16"
          />
        </svg>
      </label>
      <!-- svelte-ignore a11y-no-noninteractive-tabindex -->
      <ul
        tabindex="0"
        class="menu menu-sm dropdown-content mt-3 z-[1] p-2 shadow bg-base-100 rounded-box w-52"
      >
        <MenuLinks {menuItems} />
      </ul>
    </div>
    <a href="/" class="btn btn-ghost text-xl">TG & Y Solutions/LCL Work</a>
  </div>
  <div class="navbar-center hidden lg:flex">
    <MenuLinks {menuItems} />
  </div>
  <div class="navbar-end">
    <a href="/" class="btn">Share</a>
  </div>
</div>
