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
</script>

<svelte:head>
	<title>MUTT</title>
	<meta name="description" content="MUTT" />
</svelte:head>

<div class="cont">
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
