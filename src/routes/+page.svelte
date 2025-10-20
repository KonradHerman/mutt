<script>
  import Hero from "./_subpages/hero.svelte";
  import Work from "./_subpages/_work/work.svelte";
  import Howl from "./_subpages/howl.svelte";
  import People from "./_subpages/people.svelte";
  import Awards from "./_subpages/awards.svelte";
  import Dog from "./_subpages/dog.svelte";
  import SnapSection from "./snapSection.svelte";
  import Woof from "./_subpages/woof.svelte";
  import MobileHero from "./_subpages/mobileHero.svelte";
  import MobileWork from "./_subpages/_work/mobileWork.svelte";
  import MobileHowl from "./_subpages/mobileHowl.svelte";
  import MobilePeople from "./_subpages/mobilePeople.svelte";
  import MobileAwards from "./_subpages/mobileAwards.svelte";
  import MobileWoof from "./_subpages/mobileWoof.svelte";
  import { onMount } from "svelte";
  import Logo from "./_subpages/logo.svelte";
  // if screen is mobile sized set mobile to true
  let mobile = true;
  // if (window.innerWidth < 768) {
  // 	mobile = true
  // } else {
  // 	mobile = false
  // }
  let logoColor = "white";
  let pages = ["", "work", "howl", "people", "awards", "woof"];
  let currentPage = 1;
  let visibility = "invisible";
  let menuHeight = 0;
  let dogX = 0;
  let dogY = 0;
  let dogRect =0;
  let videoEl;
  function isInViewport(el) {
      const rect = el.getBoundingClientRect();
      return (
        rect.top >= 0 &&
        rect.left >= 0 &&
        rect.bottom <=
          (window.innerHeight || document.documentElement.clientHeight) &&
        rect.right <=
          (window.innerWidth || document.documentElement.clientWidth)
      );
    }
  function handleScroll() {
      console.log("scrolllinmg")
      if (!isInViewport(videoEl)) {
          logoColor = "black";
          visibility = "visible";
      } else {
          logoColor = "white";
          visibility = "invisible";
      }
    }
  onMount(() => {
    videoEl = document.querySelector("#heroText");
    // if screen is mobile sized set mobile to true
    if (window.innerWidth < 768) {
      mobile = true;
    } else {
      mobile = false;
    }
    // on scroll check if element is visible
    // window.addEventListener("scroll", function (event) {
    //   console.log("scroollingh");
    //   if (isInViewport(videoEl)) {
    //     logoColor = "white";
    //     visibility = "invisible";
    //   } else {
    //     logoColor = "black";
    //     visibility = "visible";
    //   }
    // });
    // setInterval(() => {
    //   if (!isInViewport(videoEl)) {
    //     logoColor = "black";
    //     visibility = "visible";
    //   } else {
    //     logoColor = "white";
    //     visibility = "invisible";
    //   }
    // }, 100);
    // window.addEventListener("scroll", function (event) {
    //   if (isInViewport(documentElement.SnapSection)) {
    //     console.log("in");
    //   } else {
    //     console.log("out");
    //   }
    // });
  });
  console.log(dogRect);
  console.log(dogX);
  console.log(logoColor);
</script>

<svelte:head>
  <title>MUTT</title>
  <meta name="description" content="MUTT" />
  <link rel="icon" type="png" href="favicon.png">
</svelte:head>

<div class="cont" on:scroll={handleScroll}>
  {#if mobile}
    <div
      class="z-40 fixed w-full h-20 align-top grid grid-cols-1 place-items-center pt-4 {logoColor}"
      bind:offsetHeight={menuHeight}
    >
      <div class="flex items-center">
        <div bind:contentRect={dogRect}
        bind:offsetWidth={dogX}>
          <svg
            id="Layer_2"
            data-name="Layer 2"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 268.31 268.31"
            class="h-20 w-20 ml-4"
          >
            <defs>
              <style>
                .cls-1 {
                  fill: currentColor;
                }

                .cls-2 {
                  stroke-width: 6.43px;
                }

                .cls-2,
                .cls-3,
                .cls-4 {
                  fill: none;
                  stroke: currentColor;
                  stroke-linecap: round;
                  stroke-linejoin: round;
                }

                .cls-3 {
                  stroke-width: 5.32px;
                }

                .cls-4 {
                  stroke-width: 5.53px;
                }
              </style>
            </defs>
            <g id="Layer_1-2" data-name="Layer 1">
              <g>
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m139.98,49.44s4.99-7.21-2.49-7.48-14.13.55-21.89,1.39c-7.76.83-22.17-.28-32.98-.28s-18.85.83-20.23,12.75c-1.39,11.92-.83,37.69.83,41.85"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m70.14,81.31c0,4.16-7.21,25.5-12.19,33.53-4.99,8.04-9.7,14.69-2.49,16.63,7.21,1.94,15.8-4.71,18.29-15.24s8.71-35.3,16.19-43.34"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m76.61,105.84c.28-1.39,9.07-30.81,17.39-39.12,8.31-8.31,14.84-12.23,23.7-13.61"
                />
                <path
                  class="cls-3 transition ease-in duration-300"
                  d="m221.96,148.67c-1.22,16.3-17.22,39.16-20.26,46.47-3.04,7.31-5.47,41.22,4.05,48.71,9.52,7.49,24.1,4.5,25.72-1.31,1.62-5.81-1.82-33.91,1.62-44.03,3.44-10.12,2.03-41.41,2.03-41.41"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m141.92,48.33s56.24-1.48,75.92,64.48c0,0,1.22,6.78,1.51,15.49"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m72.35,121.49s-3.05,9.7.55,16.63"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m114.48,71.61s15.4-5.53,18.17,6.11c0,0,1.28,11.04-2.72,15.36,0,0-11.02-3.45-14.9-10.66-3.88-7.21-.55-10.81-.55-10.81Z"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m114.12,80.86s-1.2-7.03,5.68-10.02"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m126.67,91.26c3.83-.96,2.4,5.47,5.09-7.56"
                />
                <ellipse
                  class="cls-1 transition ease-in duration-300"
                  cx="183.61"
                  cy="134.33"
                  rx="3.89"
                  ry="3.73"
                />
                <ellipse
                  class="cls-1 transition ease-in duration-300"
                  cx="124.08"
                  cy="80.21"
                  rx="3.89"
                  ry="3.73"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m117.24,108.56c-11.75,1.01-17.62,5.67-32.41,17.01-14.79,11.34-17.01,22.69-17.62,23.5,0,0-5.87,3.04-5.87,8.51s1.22,9.11,5.06,7.49c3.85-1.62,20.05-2.23,24.71,1.01,4.66,3.24,6.08-1.82,7.49-3.24,1.42-1.42,4.78-6.55,5.99-7.76"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m97.8,163.66s-2.84,3.04-.81,5.67c2.03,2.63,8.91,10.94,10.53,17.82,1.62,6.89-.41,11.14,5.87,16,6.28,4.86,10.13-.2,9.72-3.65-.41-3.44,1.22-9.52,3.65-11.14,2.43-1.62,7.29-4.46,9.32-10.13,2.03-5.67,4.05-7.29,7.7-10.74s14.58-24.51,11.95-37.07"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m102.25,136.11s-9.11-2.43-4.66-9.72c4.46-7.29,18.23-10.94,27.55-5.47,9.32,5.47,18.43,14.99,14.79,32-3.65,17.01-16,4.05-14.99,2.63"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m104.48,129.43c.81-.2,7.7-.81,7.9,6.48.2,7.29-6.48,11.14-12.15,10.13"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m128.99,149.07s-2.03-7.29-9.72-2.63c-7.7,4.66-6.89,11.34-4.25,14.38"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m64.99,165.08s-3.65,8.1,5.67,16c9.32,7.9,18.43,10.33,22.89,16.61,4.46,6.28,9.11,15.19,14.79,19.04,5.67,3.85,12.36,1.22,15.6-5.67,3.24-6.89,17.01-15.6,20.66-21.47,3.65-5.87,13.57-21.67,15.6-26.53"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m171.64,129.75s7.78-4.54,13.67-3.63c5.89.91,10.44,4.54,6.46,16.16"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m219.33,122.34s8.51-2.63,10.74,7.29c2.23,9.93,5.14,28.66,5.14,28.66"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m172.21,129.39s.38,11.08,7.41,13.8c7.03,2.72,11.39-.91,11.39-.91"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m173.54,136.29s-.38-7.08,4.37-9.44"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m187.02,143.74s5.51-2.18,6.27-8.72"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m65.61,175.14s3.04,16.76-12.55,61.94"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m132.65,107.91c1.13-.38,13.14-3.75,18.77-13.89"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m149.47,121.32c-1.88.38-1.88-9.76,10.51-20.27"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m195.66,162.07s11.68-7.68,14.07-33.07"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m129.29,59.43c-.1.23,15.6,2.2,15.87,15.87"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m172.11,113.09s14.28-7.94,23.81,4.76"
                />
                <path
                  class="cls-2 transition ease-in duration-300"
                  d="m204.56,244.58c-20.33,12.99-44.49,20.52-70.4,20.52C61.84,265.1,3.22,206.47,3.22,134.16S61.84,3.22,134.16,3.22s130.94,58.62,130.94,130.94c0,32.79-12.05,62.76-31.97,85.73"
                />
                <path
                  class="cls-4 transition ease-in duration-300"
                  d="m205.41,186.07s-3.09-13.9-10.18-16.13c-7.09-2.23-14.58,4.05-16.2,9.11-1.62,5.06-12.36,22.89-19.65,30.59s-11.75,35.24-11.55,41.73c0,0,.61,5.32,1.65,12.33"
                />
              </g>
            </g>
          </svg>
        </div>
        <div
          class="title all-round-gothic-xlig text-[5rem] leading-4 tracking-wide md:text-9xl self-center px-4 transition ease-in duration-300"
        >
          MUTT
        </div>
        
      </div>
      <!-- <div class="h-full">
        <svg class="relative left-7 transition ease-in duration-300">
          <line
            class=""
            x1="0"
            y1="0"
            x2="0"
            y2="100%"
            stroke="currentColor"
            stroke-width="4"
          />
        </svg>
      </div> -->
      <!-- hide element if in first snapsection -->
      <!-- <div>
				<p class="pl-2 text-5xl lg:text-8xl all-round-gothic-medium-oblique uppercase spacing transition ease-in duration-300 {visibility}">
					{pages[currentPage]}
				</p>
			</div> -->
    </div>
    
  {/if}
  <SnapSection id="hero">
    <div class="absolute inset-0 bg-black z-0"></div>
    <video autoplay muted loop playsinline id="myVideo" class="absolute z-10">
      <source src={mobile?"mobileVideo.mp4":"video.mp4"} type="video/mp4" />
    </video>
    {#if mobile}
      <MobileHero />
    {:else}
      <Hero />
    {/if}
  </SnapSection>

  <SnapSection id="work">
    {#if mobile}
      <MobileWork />
    {:else}
      <Work />
    {/if}
  </SnapSection>

  <SnapSection id="howl">
    {#if mobile}
      <MobileHowl />
    {:else}
      <Howl />
    {/if}
  </SnapSection>
  <SnapSection id="people">
    {#if mobile}
      <MobilePeople />
    {:else}
      <People />
    {/if}
    
  </SnapSection>
  <SnapSection id="awards">
    {#if mobile}
      <MobileAwards />
    {:else}
      <Awards />
    {/if}
    
  </SnapSection>

  <SnapSection id="woof">
    {#if mobile}
      <MobileWoof />
    {:else}
      <Woof />
    {/if}
  </SnapSection>
  <SnapSection id="dog">
    <Dog />
  </SnapSection>
</div>

<style>
  .cont {
    scroll-snap-type: y mandatory;
    overflow-y: scroll;
    overflow-x: hidden;
    height: 100vh;
  }
  video {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .white {
    color: white;
    fill: white;
    stroke: white;
  }
  .black {
    color: black;
    fill: black;
    stroke: black;
  }
  .balls {
    filter: invert(1);
  }
  .logo {
    background-color: #000;
    -webkit-mask: url(logo.svg) no-repeat center;
    mask: url(logo.svg) no-repeat center;
  }
  .align-logo {
    vertical-align: top;
  }
</style>
