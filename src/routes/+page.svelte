<script>
	import Sidebar from "./sidebar.svelte"
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="cont">
	<section class="two flex flex-col relative">
		<div class="grid grid-rows-8 h-full w-full gap-0">
			<div
				class="row-span-6 grid grid-cols-6 place-items-center w-full mt-20 relative gap-0"
			>
				<Sidebar />
				<div class=" w-full h-full border-l-4 border-b-4 border-black" />
				<div
					class="z-10 t-0 l-0 h-full absolute overlay grid grid-cols-1 place-items-center"
				>
					<div class="text-left text-9xl">
						a production <br />
						& ad agency <br />
						mongrel
					</div>
				</div>
				<div class=" w-full h-full border-b-4 border-black" />
				<div class=" w-full h-full" />
				<div class=" w-full h-full" />
				<div class=" w-full h-full" />
			</div>
			<div class="row-span-2 grid grid-cols-6 place-items-center w-full mb-20">
				<div class=" w-full h-full" />
				<div class=" w-full h-full" />
				<div class="  w-full h-full border-r-4 border-black relative">
					<div class="arrow" />
				</div>
				<div class="  w-full h-full" />
				<div class="  w-full h-full" />
				<div class="  w-full h-full" />
			</div>
		</div>
	</section>
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
	.overlay {
		width: 80%;
		margin-left: 20%;
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
	a {
		float: right;
		text-decoration: none;
		letter-spacing: 0.15em;
		width: fit-content;
		position: relative;
	}
	a:after {
		background: none repeat scroll 0 0 transparent;
		bottom: 0;
		content: "";
		display: block;
		height: 2px;
		left: 50%;
		position: absolute;
		background: black;
		transition: width 0.3s ease 0s, left 0.3s ease 0s;
		width: 0;
	}
	a:hover:after {
		width: 100%;
		left: 0;
	}
</style>
