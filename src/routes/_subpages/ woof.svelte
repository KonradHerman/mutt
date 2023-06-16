<script>
	import Sidebar from "../sidebar.svelte"
	import { fade } from "svelte/transition"
</script>

<div
	class="two flex flex-col relative text-black w-full h-full"
>
	<div class="grid grid-rows-10 h-full w-full gap-0 mt-3">
		<div
			class="row-span-1 grid grid-cols-5 place-items-center p-0 m-0"
		>
			<div class=" col-span-4 flex w-full h-full">
				<div
					class=" title all-round-gothic-xlig text-5xl lg:text-8xl flex ml-6 lg:ml-40"
				>
					<img
						src="logo-black.svg"
						class="h-10 lg:h-20 pr-4"
						alt=""
					/>
					MUTT
					<p
						class="text-5xl lg:text-8xl all-round-gothic-medium-oblique spacing"
					>
						WOOF
					</p>
				</div>
			</div>
		</div>
		<div class="center">
			<Sidebar color="black" />
			<div class=" " />
			<div
				class=" w-full h-full border-b-4 border-l-4 border-black"
			/>
			<div
				class="z-10 t-0 l-0 h-full absolute overlay flex flex-col"
			>
				<div
					class="content grid grid-cols-1 place-items-center"
				>
					<div
						class="w-full h-full grid grid-cols-1 place-items-center pl-12 text-9xl all-round-gothic-book-oblique spacing"
					>
						<div class="w-full text-left">Let's make</div>
					</div>
					<div
						class="w-full h-full grid grid-cols-1 place-items-center pl-12 text-9xl all-round-gothic-book-oblique spacing"
					>
						<div class="w-full text-left">something</div>
					</div>
					<div
						class="w-full h-full grid grid-cols-1 place-items-center pl-12 text-9xl all-round-gothic-book-oblique spacing"
					>
						<div class="w-full text-left">together.</div>
					</div>
				</div>
				<div
					class=" text-3xl all-round-gothic-book-oblique pl-12 pb-6"
				>
					<a href="mailto:woof@mutt.media"
						>Find us at <span class="underline"
							>woof@mutt.media</span
						>
					</a>
				</div>
			</div>
			<div class=" w-full h-full" />
			<div class=" w-full h-full" />
		</div>
		<div
			class="row-sdivan-3 grid grid-cols-5 divlace-items-center w-full mb-20"
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
	.spacing {
		letter-spacing: 0.2em;
		font-weight: 100;
	}
</style>
