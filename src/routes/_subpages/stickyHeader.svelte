<script>
  import Sidebar from "../sidebar.svelte";
  export let visible = false;
</script>

<div
  class="fixed top-0 left-0 h-screen z-40 transition-opacity duration-300 border-r-4 border-black {visible
    ? 'opacity-100'
    : 'opacity-0'}"
>
  <div class="flex flex-col h-full pt-3 lg:pt-6">
    <!-- Logo and MUTT inline - same size as page titles -->
    <div class="flex items-center mb-8 lg:mb-12 ml-6 lg:ml-12">
      <img src="logo-black.svg" class="h-10 lg:h-24 pr-3 lg:pr-4" alt="" />
      <div class="all-round-gothic-xlig text-5xl lg:text-8xl tracking-wide">
        MUTT
      </div>
    </div>

    <!-- Sidebar navigation - aligned with MUTT text -->
    <div class="sidebar-wrapper ml-6 lg:ml-12">
      <Sidebar color="black" />
    </div>
  </div>
</div>

<style>
  .tracking-wide {
    letter-spacing: 0.1em;
  }

  /* Override sidebar alignment to keep menu aligned with MUTT */
  .sidebar-wrapper :global(div) {
    text-align: left !important;
    align-items: flex-start !important;
    padding-right: 0 !important;
  }

  .sidebar-wrapper :global(a) {
    float: none !important;
  }
</style>
