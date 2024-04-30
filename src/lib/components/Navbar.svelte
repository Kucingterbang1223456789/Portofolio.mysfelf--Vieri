<script>
  import { Link } from "svelte-routing";
  import { handleAnchorClick } from "../../js/handleAnchorClick";

  let isHidden = true;
</script>

<nav
  class="relative z-10 rounded border border-gray-200 bg-white px-2 py-2.5 shadow sm:px-4"
>
  <div class="container mx-auto flex flex-wrap items-center justify-between">
    <a href="/" class="flex items-center">
      <span
        class="ml-2 self-center whitespace-nowrap text-xl font-semibold text-gray-700 hover:text-main-orange"
      >
        MYSELF
      </span>
    </a>

    <div class="flex items-center">
      <button
        id="menu-toggle"
        type="button"
        class="ml-3 inline-flex items-center rounded-lg p-2 text-sm text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 md:hidden"
        on:click={() => (isHidden = !isHidden)}
      >
        <span class="sr-only">Open main menu</span>
        <!-- Hamburger icon -->
        <svg
          class="h-6 w-6"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          class:openDropdown={!isHidden}
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16m-7 6h7"
          />
        </svg>
      </button>
    </div>

    <div
      class="w-full md:!block md:w-auto"
      id="mobile-menu"
      class:hideDropdown={isHidden}
    >
      <ul
        class="mt-4 flex flex-col text-lg md:mt-0 md:flex-row md:space-x-8 md:text-sm md:font-medium"
      >
        <li>
          <Link
            to="/"
            class="block rounded py-2 pl-3 pr-4 text-lg text-gray-700 hover:text-main-orange md:p-0 md:hover:bg-transparent"
          >
            Home
          </Link>
        </li>
        <li>
          <Link
            to="/gallery"
            class="block border-b border-gray-100 py-2 pl-3 pr-4 text-lg text-gray-700 hover:text-main-orange md:border-0 md:p-0 md:hover:bg-transparent"
          >
            My Gallery
          </Link>
        </li>
        <li>
          <a
            href="#contact"
            class="block border-b border-gray-100 py-2 pl-3 pr-4 text-lg text-gray-700 hover:text-main-orange md:border-0 md:p-0 md:hover:bg-transparent"
            on:click={handleAnchorClick}
          >
            Contact
          </a>
        </li>
      </ul>
    </div>
  </div>
</nav>

<style>
  .hideDropdown {
    display: none;
  }

  .openDropdown {
    stroke: #ff7904;
  }
</style>
