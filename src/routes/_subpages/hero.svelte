<script>
  import Sidebar from "../sidebar.svelte";
</script>

<div class="two flex flex-col relative text-white w-full h-full">
  <div class="grid grid-rows-10 lg:grid-rows-12 h-full w-full gap-0 mt-3">
    <div
      class="row-span-1 grid grid-cols-7 lg:grid-cols-6 place-items-center p-0 m-0 relative"
    >
      <div />
      <!-- <div />
			<div class="lg:hidden" /> -->

      <div class="z-30 absolute w-full h-full grid grid-cols-6 place-items-center">
        <div class="col-span-2 h-full flex">
          <img src="logo.svg" alt="" class="h-full" />
          <div class="title all-round-gothic-xlig text-6xl md:text-8xl">
            MUTT
          </div>
        </div>
      </div>
    </div>
    <div class="center">
      <Sidebar />
      <div class=" w-full h-full border-l-4 border-b-4 border-white" />
      <div
        class="z-10 t-0 l-0 h-full absolute overlay grid grid-cols-1 place-items-center"
      >
        <div
          class="motto all-round-gothic text-center md:text-left text-4xl sm:text-5xl md:text-5xl xl:text-6xl"
        >
          <div class="grid-query h-full">
            <p class="p-8 pl-0">an ad agency</p>
            <p class="p-8 pl-0">& production</p>
            <p class="p-8 pl-0 pb-0">mongrel</p>
          </div>
        </div>
      </div>
      <div class=" w-full h-full border-b-4 border-white" />
      <div class=" w-full h-full" />
      <div class=" w-full h-full" />
      <div class=" w-full h-full" />
    </div>
    <div
      class="row-span-3 lg:row-span-5 grid grid-cols-6 place-items-center w-full mb-2"
    >
      <div class=" w-full h-full" />
      <div class=" w-full h-full" />
      <div class="  w-full h-full border-r-4 border-white relative min-h-6">
        <div class="arrow" />
      </div>
      <div class="  w-full h-full" />
      <div class="  w-full h-full" />
      <div class="  w-full h-full" />
    </div>
  </div>
</div>

<style lang="postcss" scoped>
  .center {
    @apply row-span-6 grid grid-cols-6 place-items-center w-full relative gap-0 h-full;
  }
  .motto {
    letter-spacing: 0.4em;
    @apply w-full h-5/6 flex flex-col justify-end font-bold;
  }
  .overlay {
    width: 80%;
    margin-left: 20%;
  }
  .arrow {
    width: 50px;
    height: 50px;
    border-left: 4px solid white;
    border-bottom: 4px solid white;
    transform: rotate(315deg);
    right: -2px;
    bottom: 5px;
    translate: 50%;
    position: absolute;
  }
  .title {
    letter-spacing: 0.1em;
  }
  @media (max-width: 768px) {
    .grid-query {
      /* Change the grid to a single column on small screens. */
      grid-template-columns: 1fr;
      justify-items: stretch;
      align-items: stretch;
    }
  }
  @media (max-width: 1024px) {
    .arrow {
      width: 25px;
      height: 25px;
    }
  }
</style>
