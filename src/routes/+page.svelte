<script>
	import Hero from "./hero.svelte"
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="cont">
	<Hero />
	<section class="one">
		<h1 class="h1 text-9xl">MUTT</h1>
	</section>

	<section class="three">
		<h1>three</h1>
	</section>
	<section class="four">
		<h1>four</h1>
	</section>
	<section class="five">
		<h1>five</h1>
	</section>
	<section class="six">
		<h1>six</h1>
	</section>
	<section class="seven">
		<h1>seven</h1>
	</section>
	<section class="eight">
		<h1>eight</h1>
	</section>
</div>

<style>
	.cont {
		scroll-snap-type: y mandatory;
		overflow-y: scroll;
		overflow-x: hidden;
		height: 100vh;
	}
	section {
		height: 100vh;
		display: flex;
		justify-content: center;
		align-items: center;
		scroll-snap-align: start;
	}
	h1 {
		color: black;
	}
</style>
