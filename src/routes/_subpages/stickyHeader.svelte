<script>
  import Sidebar from "../sidebar.svelte";
  export let visible = false;
</script>

<div
  class="fixed top-0 left-0 w-full h-auto z-50 transition-opacity duration-300 pointer-events-none {visible
    ? 'opacity-100'
    : 'opacity-0'}"
>
  <div class="grid grid-cols-5 w-full gap-0 mt-3 pointer-events-auto">
    <!-- Logo and MUTT title -->
    <div class="col-span-4 flex w-full h-full">
      <div
        class="all-round-gothic-xlig text-5xl lg:text-8xl flex ml-6 lg:ml-40 items-center"
      >
        <img src="logo-black.svg" class="h-10 lg:h-24 pr-4" alt="" />
        <span class="tracking-wide">MUTT</span>
      </div>
    </div>
    <!-- Sidebar navigation -->
    <div class="col-span-1 flex items-start justify-end pt-2">
      <Sidebar color="black" />
    </div>
  </div>
</div>

<style>
  .tracking-wide {
    letter-spacing: 0.1em;
  }
</style>
