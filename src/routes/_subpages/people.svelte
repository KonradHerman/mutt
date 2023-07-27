<script>
  import Sidebar from "../sidebar.svelte";
  import { fade } from "svelte/transition";
</script>

<div class="two flex flex-col relative text-black w-full h-full">
  <div class="grid grid-rows-10 h-full w-full gap-0 mt-3">
    <div class="row-span-1 grid grid-cols-5 place-items-center p-0 m-0">
      <div class=" col-span-4 flex w-full h-full">
        <div
          class=" title all-round-gothic-xlig text-5xl lg:text-8xl flex ml-6 lg:ml-40"
        >
          <img src="logo-black.svg" class="h-10 lg:h-24 pr-4" alt="" />
          MUTT
          <p
            class="text-5xl lg:text-8xl all-round-gothic-medium-oblique spacing"
          >
            PEOPLE
          </p>
        </div>
      </div>
    </div>
    <div class="center">
      <div class="col-span-1 -z-10" />
      <div class="absolute text-9xl w-full h-full grid grid-cols-5">
        <Sidebar color="black" />
        <div class="col-span-2 grid grid-cols-1 place-items-center pb-20">
          <div class="w-20">
            <img
              src="pics/kiko.jpg"
              alt="kiko"
              class="rounded-full border-4 border-black "
            />
          </div>
          <div class="w-20">
            <img
              src="pics/Dave.JPG"
              alt="dave"
              class="rounded-full border-4 border-black"
            />
          </div>
        </div>
      </div>
      <div
        class=" w-full h-full grid grid-rows-2 text-xl md:text-4xl lg:text-5xl text-right pr-4 open-sans"
      >
        <div class="w-full h-full grid grid-cols-1 place-items-end pb-2">
          <div class="  w-full">
            <p>Kiko</p>
            <p>Mattoso</p>
          </div>
        </div>
        <div class="w-full h-full grid grid-cols-1 place-items-end pb-2">
          <div class="  w-full">
            <p>Dave</p>
            <p>Herman</p>
          </div>
        </div>
      </div>
      <div class=" w-full h-full border-b-4 border-l-4 border-black" />
      <div
        class="z-10 t-0 l-0 h-full absolute overlay grid grid-cols-1 place-items-center"
      >
        <div class="content open-sans">
          <div class=" w-full h-full grid grid-rows-2 pr-4">
            <div class="w-full h-full grid grid-cols-1 place-items-end pb-6">
              <div class="  w-full pl-12">
                <p>
                  More than 20 years working in the ad world creating ideas for
                  brands such as Tide, Mastercard, Volkswagen, GM, McDonald's,
                  Burger King, Dial, Stella Artois and others
                </p>
              </div>
            </div>
            <div class="w-full h-full grid grid-cols-1 place-items-end pb-6">
              <div class="  w-full pl-12">
                <p>
                  Brings 25 years production experience from Verizon,
                  Mastercard, MGM, BMW, NY Lottery, Microsoft, Levis, Absolut
                  and many many others. He is well versed in every phase of
                  every type of production and post production
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class=" w-full h-full" />
      <div class=" w-full h-full" />
    </div>
    <div class="row-span-3 grid grid-cols-5 place-items-center w-full mb-20">
      <div class=" w-full h-full" />
      <div class=" w-full h-full" />
      <div class="  w-full h-full border-r-4 border-black relative">
        <div class="arrow" />
      </div>
      <div class="  w-full h-full" />
      <div class="  w-full h-full" />
    </div>
  </div>
</div>

<style lang="postcss" scoped>
  .center {
    @apply row-span-6 grid grid-cols-5 place-items-center w-full relative gap-0 h-full;
  }
  .content {
    letter-spacing: 0.1em;
    @apply text-justify text-sm lg:text-lg xl:text-xl w-full h-full flex flex-col justify-end font-bold pr-20;
  }
  .overlay {
    width: 60%;
    margin-left: 40%;
  }
  .arrow {
    width: 50px;
    height: 50px;
    border-left: 4px solid black;
    border-bottom: 4px solid black;
    transform: rotate(315deg);
    right: -2px;
    bottom: 5px;
    translate: 50%;
    position: absolute;
  }
  .title {
    letter-spacing: 0.1em;
    @apply row-span-5  w-full h-full;
  }
  @media (max-width: 550px) {
    .content {
      font-size: 0.7rem;
    }
  }
</style>
