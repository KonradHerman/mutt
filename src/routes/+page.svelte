<script>
	import Hero from "./_subpages/hero.svelte"
	import Work from "./_subpages/_work/work.svelte"
	import Howl from "./_subpages/howl.svelte"
	import People from "./_subpages/people.svelte"
	import Awards from "./_subpages/awards.svelte"
	import Dog from "./_subpages/dog.svelte"
	import SnapSection from "./snapSection.svelte"
	import Woof from "./_subpages/ woof.svelte"
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
