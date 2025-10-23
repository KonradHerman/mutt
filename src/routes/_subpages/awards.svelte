<script>
	import Sidebar from "../sidebar.svelte"
	import { fade } from "svelte/transition"
</script>

<div
	class="two flex flex-col relative text-black w-full h-full"
>
	<div class="grid grid-rows-10 h-full w-full gap-0">
		<div
			class="row-span-1 grid grid-cols-5 place-items-center p-0 m-0 pt-3 lg:pt-6"
		>
			<div class="col-span-4 flex w-full h-full items-center">
				<div class="page-title all-round-gothic-medium-oblique text-5xl lg:text-8xl ml-6 lg:ml-12">
					AWARDS
				</div>
			</div>
		</div>
		<div class="center">
			<div class="w-full h-full" />
			<div
				class=" w-full h-full grid grid-cols-2 grid-flow-row place-items-center text-5xl p-6"
			>
				<div
					class=" h-full w-full grid grid-cols-1 place-items-center"
				>
					<img src="awards/1.gif" alt="" class="h-20" />
				</div>
				<div
					class=" h-full w-full grid grid-cols-1 place-items-center"
				>
					<img src="awards/2.png" alt="" class="h-20" />
				</div>
				<div
					class=" h-full w-full grid grid-cols-1 place-items-center"
				>
					<img src="awards/3.png" alt="" class="h-10" />
				</div>
				<div
					class=" h-full w-full grid grid-cols-1 place-items-center"
				>
					<img src="awards/4.png" alt="" class="h-8" />
				</div>
				<div
					class=" h-full w-full grid grid-cols-1 place-items-center"
				>
					<img src="awards/5.jpg" alt="" class="h-16" />
				</div>
				<div
					class=" h-full w-full grid grid-cols-1 place-items-center"
				>
					<img src="awards/6.jpg" alt="" class="h-12" />
				</div>
				<div
					class=" h-full w-full grid grid-cols-1 place-items-center"
				>
					<img src="awards/7.jpeg" alt="" class="h-20" />
				</div>
				<div
					class=" h-full w-full grid grid-cols-1 place-items-center"
				>
					<img src="awards/8.jpg" alt="" class="h-20" />
				</div>
			</div>
			<div
				class=" w-full h-full border-b-4 border-l-4 border-black"
			/>
			<div
				class="z-10 t-0 l-0 h-full absolute overlay grid grid-cols-1 place-items-center"
			>
				<div class="content">
					<div
						class="grid grid-rows-9 place-items-center h-full w-full text-left pb-6 pl-6 open-sans text-2xl"
					>
						<div class="min-w-full">
							Mutts have won all major
						</div>
						<div class="min-w-full">
							awards in the industry,
						</div>
						<div class="min-w-full">
							such as the Film Grand Prix
						</div>
						<div class="min-w-full">at Cannes Lions,</div>
						<div class="min-w-full">
							the D&AD Black Pencil
						</div>
						<div class="min-w-full">
							the Grand Clio among many others
						</div>
					</div>
				</div>
			</div>
			<div class=" w-full h-full" />
			<div class=" w-full h-full" />
		</div>
		<div
			class="row-span-3 grid grid-cols-5 place-items-center w-full mb-20"
		>
			<div class=" w-full h-full" />
			<div class=" w-full h-full" />
			<div
				class="  w-full h-full border-r-4 border-black relative"
			>
				<div class="arrow" />
			</div>
			<div class="  w-full h-full" />
			<div class="  w-full h-full" />
		</div>
	</div>
</div>

<style lang="postcss" scoped>
	.center {
		@apply row-span-6 grid grid-cols-5 place-items-center w-full relative gap-0 h-full;
	}
	.content {
		letter-spacing: 0.1em;
		@apply text-justify text-xl w-full h-full flex flex-col justify-end font-bold pr-20;
	}
	.overlay {
		width: 60%;
		margin-left: 40%;
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
	.title {
		letter-spacing: 0.1em;
		@apply row-span-5  w-full h-full;
	}
	.page-title {
		letter-spacing: 0.1em;
	}
	.tracking-wide {
		letter-spacing: 0.1em;
	}
</style>
