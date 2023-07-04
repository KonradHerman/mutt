<script>
	import Sidebar from "../sidebar.svelte"
</script>

<div class="z-10 flex  w-full h-full absolute">
	<div class=" w-full h-20 text-white align-top mx-4 grid grid-cols-1 place-items-center bg-red-500">

			<div class="flex h-full w-full items-center">
					<img src="logo.svg" alt="" class="h-20 col-span-1 align-top" />
					<div class="title all-round-gothic-xlig text-[5rem] md:text-8xl self-center px-4">MUTT
				</div>
	

		</div>
	</div>
</div>

<style lang="postcss" scoped>
	.center {
		@apply row-span-6 grid grid-cols-6 place-items-center w-full relative gap-0 h-full;
	}
	.motto {
		letter-spacing: 0.4em;
		@apply w-full h-5/6 flex flex-col justify-end font-bold;
	}
	.overlay {
		width: 80%;
		margin-left: 20%;
	}
	.arrow {
		width: 50px;
		height: 50px;
		border-left: 4px solid white;
		border-bottom: 4px solid white;
		transform: rotate(315deg);
		right: -2px;
		bottom: 5px;
		translate: 50%;
		position: absolute;
	}
	.title {
		letter-spacing: 0.1em;
	}
	@media (max-width: 768px) {
		.grid-query {
			/* Change the grid to a single column on small screens. */
			grid-template-columns: 1fr;
			justify-items: stretch;
			align-items: stretch;
		}
	}
	@media (max-width: 1024px) {
		.arrow {
			width: 25px;
			height: 25px;
		}
	}
</style>
