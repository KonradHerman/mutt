<script>
  import Sidebar from "../../sidebar.svelte";
  import { content } from "./content.js";
  import { fade } from "svelte/transition";
  let activeContent = false;
  const activate = (key) => () => {
    activeContent = false;
    setTimeout(() => {
      activeContent = content[key];
    }, 10);
  };
  let showMaximizeButton = false;
  let showMinimizeButton = false;
  let maximized = false;
  const maximize = () => {
    maximized = true;
  };
  const minimize = () => {
    maximized = false;
  };
</script>

<div class="two flex flex-col relative text-black w-full h-full">
  {#if maximized}
    <div
      class="align-top w-full h-full absolute z-40 grid grid-cols-5 place-items-center"
      transition:fade={{ duration: 700 }}
    >
      <div />
      <div class="col-span-4 w-full h-full">
        <div class="flex flex-col items-center justify-center w-full h-full">
          <div
            class="w-full h-2/3 z-50 relative"
            on:mouseenter={() => {
              showMinimizeButton = true;
            }}
            on:mouseleave={() => {
              showMinimizeButton = false;
            }}
          >
			
				<iframe
				  src={"https://player.vimeo.com/video/" + value.video + "?h=70d246fdb6&autoplay=1&title=0&byline=0&portrait=0"}
				  style="position:absolute;top:0;left:0;width:100%;height:100%;"
				  frameborder="0"
				  allow="autoplay; fullscreen; picture-in-picture"
				  allowfullscreen
				/>
			  <script src="https://player.vimeo.com/api/player.js"></script>
            {#if showMinimizeButton}
              <div class="absolute inset-0 grid grid-cols-1 place-items-center">
                <div
                  class=" maximize text-center rounded-full border-4 hover:shadow-2xl hover:shadow-white cursor-pointer transition-all duration-500 ease-in-out"
                  transition:fade={{ duration: 700 }}
                >
                  <img
                    src="minimize.svg"
                    alt=""
                    class="h-12 p-2"
                    on:click={minimize}
                  />
                </div>
              </div>
            {/if}
          </div>
        </div>
      </div>
    </div>
  {/if}
  <div class="grid grid-rows-10 h-full w-full gap-0 mt-20 lg:mt-32">
    <div class="row-span-1 grid grid-cols-5 place-items-center p-0 m-0">
      <div class=" col-span-4 flex w-full h-full">
        <div
          class=" page-title all-round-gothic-medium-oblique text-5xl lg:text-8xl flex ml-6 lg:ml-40"
        >
          WORK
        </div>
      </div>
    </div>

    <div class="center {maximized ? 'text-white' : ''}">
      <div class="w-full h-full" />

      <div class=" w-full h-full content flex flex-col items-center">
        {#if activeContent}
          <div
            class="align-top w-full h-1/3 xl:h-1/2 relative"
            on:mouseenter={() => {
              showMaximizeButton = true;
            }}
            on:mouseleave={() => {
              showMaximizeButton = false;
            }}
          >
            {#if !maximized}
              <div class="w-full h-full">
                <iframe
                  src={"https://player.vimeo.com/video/" +
                    activeContent.video +
                    "?h=70d246fdb6&title=0&byline=0&portrait=0"}
                  frameborder="0"
                  allow="autoplay; fullscreen"
                  class="w-full p-0 m-0 h-full"
                  allowfullscreen
                />
              </div>
              <script src="https://player.vimeo.com/api/player.js"></script>
            {/if}
          </div>

          <div class="w-full h-2/3 xl:h-1/2">
            <p
              in:fade={{ duration: 700 }}
              class=" text-left p-1 pb-0 pl-0 mb-0  h-full open-sans weight work-content text-9xl" 
            >
              {@html activeContent.text}
              <br />
			  <br />
              <span class="font-extrabold open-sans">
                {activeContent.end}
              </span>
            </p>
          </div>
        {/if}
      </div>
      <div
        class=" w-full h-full border-b-4 border-l-4 border-black {maximized
          ? 'border-white'
          : ''}"
      />
      <div
        class="z-10 t-0 l-0 h-full absolute overlay grid grid-cols-1 place-items-center"
      >
        <div class="motto">
          <div
            class="grid grid-cols-1 place-items-left h-full pb-6 open-sans"
          >
            {#each Object.entries(content) as [key, value]}
              <div class="content-link" on:mouseenter={activate(key)}>
                {key}
              </div>
            {/each}
          </div>
        </div>
      </div>
      <div class=" w-full h-full" />
      <div class=" w-full h-full" />
    </div>
    <div class="row-span-3 grid grid-cols-5 place-items-center w-full mb-20">
      <div class=" w-full h-full" />
      <div class=" w-full h-full" />
      <div
        class="  w-full h-full border-r-4 border-black {maximized
          ? 'border-white'
          : ''} relative"
      >
        <div class="arrow {!maximized ? 'arrowVisible' : ''}" />
      </div>
      <div class="  w-full h-full" />
      <div class="  w-full h-full" />
    </div>
  </div>
</div>

<style lang="postcss" scoped>
  .content-link {
    @apply py-1 ml-5 pl-0 cursor-pointer uppercase;
  }
  .center {
    @apply row-span-6 grid grid-cols-5 place-items-center w-full relative gap-0 h-full;
  }
  .motto {
    letter-spacing: 0.1em;
    @apply text-left text-4xl w-full h-full flex flex-col justify-end font-bold;
  }
  .spacing {
    letter-spacing: 0.1em;
  }
  .overlay {
    width: 60%;
    margin-left: 40%;
  }
  .arrow {
    width: 50px;
    height: 50px;

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
  .page-title {
    letter-spacing: 0.1em;
  }
  a {
    float: left;
    text-decoration: none;
    letter-spacing: 0.15em;
    width: fit-content;
    position: relative;
  }
  a:after {
    background: none repeat scroll 0 0 transparent;
    bottom: 30px;
    content: "";
    display: block;
    height: 2px;
    left: 50%;
    position: absolute;
    background: black;
    transition: width 0.3s ease 0s, left 0.3s ease 0s;
    width: 0;
  }
  @media screen and (max-height: 865px) {
    a:after {
      bottom: 10px;
    }
  }
  a:hover:after {
    width: 100%;
    left: 0;
  }
  .weight {
    letter-spacing: 0.1em;
    font-weight: 100;
  }
  .work-content {
    font-size: 1rem;
  }
  @media (max-width: 1300px) {
    .work-content {
      font-size: 1rem;
    }
  }
  @media (max-width: 1024px) {
    .work-content {
      font-size: 0.8rem;
    }
  }
  @media (max-width: 800px) {
    .work-content {
      font-size: 0.7rem;
    }
  }
  @media (max-width: 680px) {
    .work-content {
      font-size: 0.65rem;
    }
  }
  @media (max-width: 600px) {
    .work-content {
      font-size: 0.5rem;
    }
  }
  @media (max-width: 1024px) {
    .arrow {
      width: 25px;
      height: 25px;
			bottom: 3px;
    }
  }
  .arrowVisible {
    border-left: 4px solid black;
    border-bottom: 4px solid black;
  }
  .maximize:hover {
    background: rgba(120, 119, 119, 0.529);
  }
</style>
