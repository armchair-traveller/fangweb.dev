<script>
  import { slide } from "svelte/transition";
  var opened = false;
</script>

<style>
  /* Burger */
  .line {
    fill: none;
    stroke: black;
    stroke-width: 6;
    transition: stroke-dasharray 600ms cubic-bezier(0.4, 0, 0.2, 1),
      stroke-dashoffset 600ms cubic-bezier(0.4, 0, 0.2, 1);
  }

  .line1,
  .line3 {
    stroke-dasharray: 60 207;
  }
  .line2 {
    stroke-dasharray: 60 60;
  }

  .opened .line1,
  .opened .line3 {
    stroke-dasharray: 90 207;
    stroke-dashoffset: -134;
  }
  .opened .line2 {
    stroke-dasharray: 1 60;
    stroke-dashoffset: -30;
  }

  menu a {
    padding-bottom: 1rem;
    font-weight: 600;
  }
</style>

<header
  class="mt-8 px-6 flex flex-nowrap flex-row justify-between items-center">
  <a class="font-semibold text-xl" href="/">Fang🦁</a>
  <button
    class="bg-transparent border-none cursor-pointer flex p-0 h-full hover:bg-gray-100 md:hidden"
    class:opened
    aria-expanded={opened}
    on:click={() => (opened = !opened)}
    aria-label="Main Menu">
    <!-- prettier-ignore -->
    <svg width="35" height="35" viewBox="0 0 100 100">
      <path class="line line1" d="M 20,29.000046 H 80.000231 C 80.000231,29.000046 94.498839,28.817352 94.532987,66.711331 94.543142,77.980673 90.966081,81.670246 85.259173,81.668997 79.552261,81.667751 75.000211,74.999942 75.000211,74.999942 L 25.000021,25.000058" />
      <path class="line line2" d="M 20,50 H 80" />
      <path class="line line3" d="M 20,70.999954 H 80.000231 C 80.000231,70.999954 94.498839,71.182648 94.532987,33.288669 94.543142,22.019327 90.966081,18.329754 85.259173,18.331003 79.552261,18.332249 75.000211,25.000058 75.000211,25.000058 L 25.000021,74.999942" />
    </svg>
  </button>
</header>

{#if opened}
  <menu class="flex flex-col mb-0" transition:slide={{ y: -30, duration: 200 }}>
    <a href="#">Projects</a>
    <a rel="external" href="https://github.com/armchair-traveller">GitHub</a>
  </menu>
{/if}
