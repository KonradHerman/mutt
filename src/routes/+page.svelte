<script>
	import Hero from "./hero.svelte"
	import SnapSection from "./snapSection.svelte"
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="cont">
	<SnapSection>
		<Hero />
	</SnapSection>

	<SnapSection>
		<h1 class="h1 text-9xl">MUTT</h1>
	</SnapSection>

	<SnapSection>
		<h1>three</h1>
	</SnapSection>
	<SnapSection>
		<h1>four</h1>
	</SnapSection>
	<SnapSection>
		<h1>five</h1>
	</SnapSection>
	<SnapSection>
		<h1>six</h1>
	</SnapSection>
	<SnapSection>
		<h1>seven</h1>
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
</style>
