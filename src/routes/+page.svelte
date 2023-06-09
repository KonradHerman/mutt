<script>
	import Hero from "./_subpages/hero.svelte"
	import Work from "./_subpages/_work/work.svelte"
	import Howl from "./_subpages/howl.svelte"
	import People from "./_subpages/people.svelte"
	import Dog from "./_subpages/dog.svelte"
	import SnapSection from "./snapSection.svelte"
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="cont">
	<SnapSection>
		<video
			autoplay
			muted
			loop
			id="myVideo"
			class="absolute z-100"
		>
			<source src="video.mp4" type="video/mp4" />
		</video>
		<Hero />
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
	<SnapSection id="dog">
		<Dog />
	</SnapSection>
	<SnapSection>
		<img src="SVG_DOGS/Asset 5.svg" width="20%" />
	</SnapSection>
	<SnapSection>
		<img src="SVG_DOGS/Asset4.svg" width="20%" />
	</SnapSection>

	<SnapSection>
		<h1>eight</h1>
	</SnapSection>
</div>

<style>
	.cont {
		scroll-snap-type: y mandatory;
		overflow-y: scroll;
		overflow-x: hidden;
		height: 100vh;
	}

	h1 {
		color: black;
	}
	video {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
</style>
