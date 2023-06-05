<script>
	import Sidebar from "./sidebar.svelte"
</script>

<section class="two flex flex-col relative">
	<div class="grid grid-rows-10 h-full w-full gap-0">
		<div class="row-span-1" />
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
		<div class="row-span-3 grid grid-cols-6 place-items-center w-full mb-20">
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

<style>
	section {
		height: 100vh;
		display: flex;
		justify-content: center;
		align-items: center;
		scroll-snap-align: start;
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
</style>
