<script>
  import Sidebar from "../sidebar.svelte";
  export let visible = false;
  export let currentPage = "";
</script>

<div
  class="fixed top-0 left-0 h-screen z-40 transition-opacity duration-300 {visible
    ? 'opacity-100'
    : 'opacity-0'}"
>
  <div class="flex flex-col h-full pt-3 lg:pt-6 pl-6 lg:pl-12">
    <!-- Logo, MUTT, and Page Title inline -->
    <div class="flex items-center mb-8 lg:mb-12">
      <img src="logo-black.svg" class="h-10 lg:h-16 pr-3 lg:pr-4" alt="" />
      <div class="all-round-gothic-xlig text-4xl lg:text-6xl tracking-wide">
        MUTT
      </div>
      {#if currentPage}
        <div class="all-round-gothic-medium-oblique text-4xl lg:text-6xl tracking-wide ml-0">
          {currentPage}
        </div>
      {/if}
    </div>

    <!-- Sidebar navigation -->
    <div>
      <Sidebar color="black" />
    </div>
  </div>
</div>

<style>
  .tracking-wide {
    letter-spacing: 0.1em;
  }
</style>
