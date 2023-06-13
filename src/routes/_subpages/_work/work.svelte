<script>
	import Sidebar from "../../sidebar.svelte"
	import { content } from "./content.js"
	import { fade } from "svelte/transition"
	let activeContent = false
	const activate = key => () => {
		activeContent = false
		setTimeout(() => {
			activeContent = content[key]
		}, 10)
	}
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
					class=" title all-round-gothic-xlig text-5xl lg:text-8xl flex ml-6 lg:ml-80"
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
						WORK
					</p>
				</div>
			</div>
		</div>
		<div class="center">
			<Sidebar color="black" />
			<div
				class=" w-full h-full content flex flex-col items-center"
			>
				{#if activeContent}
					<div class="align-top w-full h-1/3 lg:h-1/2">
						<iframe
							src={activeContent.video}
							frameborder="0"
							allow="autoplay; picture-in-picture"
							allowfullscreen
							class="w-full p-0 m-0 h-full"
							in:fade={{ duration: 700 }}
						/>
					</div>
					<div class="w-full h-2/3 lg:h-1/2">
						<p
							in:fade={{ duration: 700 }}
							class="text-justify p-1 md:p-4 pb-0 pl-0 mb-0 max-h-44 all-round-gothic-book-oblique weight work-content"
						>
							{@html activeContent.text}
						</p>
					</div>
				{/if}
			</div>
			<div
				class=" w-full h-full border-b-4 border-l-4 border-black"
			/>
			<div
				class="z-10 t-0 l-0 h-full absolute overlay grid grid-cols-1 place-items-center"
			>
				<div class="motto">
					<div
						class="grid grid-cols-1 place-items-left h-full pb-6 all-round-gothic-xlig-oblique"
					>
						<a
							class="content-link"
							on:mouseenter={activate("tide")}>TIDE AD</a
						>
						<a
							class="content-link"
							on:mouseenter={activate("got2be")}>Göt2b</a
						>
						<a
							class="content-link"
							on:mouseenter={activate("olay")}>OLAY</a
						>
						<a
							class="content-link"
							on:mouseenter={activate("neom")}>NEOM</a
						>
						<a
							class="content-link"
							on:mouseenter={activate("verizon")}>VERIZON</a
						>
						<a
							class="content-link"
							on:mouseenter={activate("bellagio")}
							>BELLAGIO</a
						>
						<!-- <a class="content-link">NEOM BILLBOARD</a> -->
						<a
							class="content-link"
							on:mouseenter={activate("donateLife")}
							>DONATE LIFE</a
						>
						<a
							class="content-link"
							on:mouseenter={activate("metaverse")}
							>METAVERSE</a
						>
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
	.content-link {
		@apply py-1 ml-5 pl-0 cursor-pointer uppercase;
	}
	.center {
		@apply row-span-6 grid grid-cols-5 place-items-center w-full relative gap-0 h-full;
	}
	.motto {
		letter-spacing: 0.1em;
		@apply text-left text-4xl w-full h-full flex flex-col justify-end font-bold;
	}
	.spacing {
		letter-spacing: 0.1em;
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
	a {
		float: left;
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
	.weight {
		letter-spacing: 0.1em;
		font-weight: 100;
	}
	.work-content {
		font-size: 0.8rem;
	}
	@media (max-width: 1300px) {
		.work-content {
			font-size: 0.7rem;
		}
	}
	@media (max-width: 1024px) {
		.work-content {
			font-size: 0.65rem;
		}
	}
	@media (max-width: 800px) {
		.work-content {
			font-size: 0.6rem;
		}
	}
	@media (max-width: 680px) {
		.work-content {
			font-size: 0.55rem;
		}
	}
	@media (max-width: 600px) {
		.work-content {
			font-size: 0.5rem;
		}
	}
	@media (max-width: 1024px) {
		.arrow {
			width: 25px;
			height: 25px;
		}
	}
</style>
