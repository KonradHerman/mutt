<script>
	import Hero from "./_subpages/hero.svelte"
	import Work from "./_subpages/_work/work.svelte"
	import Howl from "./_subpages/howl.svelte"
	import People from "./_subpages/people.svelte"
	import Awards from "./_subpages/awards.svelte"
	import Dog from "./_subpages/dog.svelte"
	import SnapSection from "./snapSection.svelte"
	import Woof from "./_subpages/woof.svelte"
	import MobileHero from "./_subpages/mobileHero.svelte"
  	import { onMount } from "svelte";
	// if screen is mobile sized set mobile to true
	let mobile = true
	// if (window.innerWidth < 768) {
	// 	mobile = true
	// } else {
	// 	mobile = false
	// }
	onMount (() => {
		// if screen is mobile sized set mobile to true
		if (window.innerWidth < 768) {
			mobile = true
		} else {
			mobile = false
		}
		console.log(mobile)
		console.log(window.innerWidth)
	})


	function isInViewport(el) {
    const rect = el.getBoundingClientRect();
    	return (
        	rect.top >= 0 &&
       		rect.left >= 0 &&
        	rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
        	rect.right <= (window.innerWidth || document.documentElement.clientWidth)
    	);
	}

const hero = document.querySelector('#myVideo');
isInViewport(box) 

</script>

<svelte:head>
	<title>MUTT</title>
	<meta name="description" content="MUTT" />
</svelte:head>



<div class="cont ">
	{#if mobile}
		<div class="z-10 fixed w-full h-20 text-white align-top mx-4 grid grid-cols-1 place-items-center pt-4">
		
			<div class="flex items-center">
				<img src="logo.svg" alt="" class="h-20  col-span-1 align-top" />
				<div class="title all-round-gothic-xlig text-[5rem] leading-4 tracking-wide md:text-9xl self-center px-4">MUTT</div>
			</div>	
		</div>
	{/if}
		
	<SnapSection>
		<video
			autoplay
			muted
			loop
			id="myVideo"
			class="absolute z-0"
		>
			<source src="video.mp4" type="video/mp4" />
		</video>
		{#if mobile}
			<MobileHero />
			<div>Hi</div>
		{:else}
			<Hero />
		{/if}
		
	</SnapSection>

	<SnapSection id="work">
		<Work />
	</SnapSection>

	<SnapSection id="howl">
		<Howl />
	</SnapSection>
	<SnapSection id="people">
		<People />
	</SnapSection>
	<SnapSection id="awards">
		<Awards />
	</SnapSection>

	<SnapSection id="woof">
		<Woof />
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
</style>
