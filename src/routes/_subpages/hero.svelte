<script>
	import Sidebar from "../sidebar.svelte"
</script>

<div
	class="two flex flex-col relative text-white w-full h-full z-50"
>
	<div class="grid grid-rows-10 h-full w-full gap-0 mt-4">
		<div
			class="row-span-1 grid grid-cols-12 place-items-center p-0 m-0 relative"
		>
			<div />
			<div class="col-span-2 h-full">
				<img src="logo-white.png" alt="" class="h-full" />
			</div>
			<div class=" w-full col-span-4 title all-round-gothic-xlig z-50 text-left">
				MUTT
			</div>
		</div>
		<div class="center">
			<Sidebar />
			<div
				class=" w-full h-full border-l-4 border-b-4 border-white z-50"
			/>
			<div
				class="z-10 t-0 l-0 h-full absolute overlay grid grid-cols-1 place-items-center"
			>
				<div class="motto all-round-gothic">
					<div>
						<p class="p-8 pl-0">a production</p>
						<p class="p-8 pl-0">& ad agency</p>
						<p class="p-8 pl-0 pb-0">mongrel</p>
					</div>
				</div>
			</div>
			<div
				class=" w-full h-full border-b-4 border-white z-50"
			/>
			<div class=" w-full h-full" />
			<div class=" w-full h-full" />
			<div class=" w-full h-full" />
		</div>
		<div
			class="row-span-3 grid grid-cols-6 place-items-center w-full mb-20"
		>
			<div class=" w-full h-full" />
			<div class=" w-full h-full" />
			<div
				class="  w-full h-full border-r-4 border-white relative"
			>
				<div class="arrow" />
			</div>
			<div class="  w-full h-full" />
			<div class="  w-full h-full" />
			<div class="  w-full h-full" />
		</div>
	</div>
</div>

<style lang="postcss" scoped>
	.center {
		@apply row-span-6 grid grid-cols-6 place-items-center w-full relative gap-0 h-full;
	}
	.motto {
		letter-spacing: 0.3em;
		@apply text-left text-8xl w-full h-full flex flex-col justify-end font-bold;
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
		font-size: 11rem;
		letter-spacing: 0.1em;
	}
</style>
