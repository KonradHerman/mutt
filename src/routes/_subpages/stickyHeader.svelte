<script>
  import Sidebar from "../sidebar.svelte";
  export let visible = false;
</script>

<div
  class="fixed top-0 left-0 h-screen z-40 transition-opacity duration-300 {visible
    ? 'opacity-100'
    : 'opacity-0'}"
>
  <div class="flex flex-col h-full pt-6 pl-6 lg:pl-12">
    <!-- Logo -->
    <div class="mb-4">
      <img src="logo-black.svg" class="h-10 lg:h-16" alt="" />
    </div>

    <!-- MUTT title -->
    <div class="mb-8 lg:mb-12">
      <div class="all-round-gothic-xlig text-4xl lg:text-6xl tracking-wide">
        MUTT
      </div>
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
