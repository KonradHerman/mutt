<script>
	import Sidebar from "../../sidebar.svelte"
	import { content } from "./content.js"
	import { fade } from "svelte/transition"
	let activeContent = false
	const activate = key => () => {
		activeContent = false
		setTimeout(() => {
			activeContent = content[key]
		}, 500)
	}
</script>

<div class="two flex flex-col relative text-black w-full h-full">
	<div class="grid grid-rows-10 h-full w-full gap-0 mt-3">
		<div class="row-span-1 grid grid-cols-5 place-items-center p-0 m-0">
			<div />
			<div class="title">MUTT</div>
		</div>
		<div class="center">
			<Sidebar color="black" />
			<div class=" w-full h-full content flex flex-col items-center">
				{#if activeContent}
					<iframe
						in:fade={{ duration: 2500 }}
						out:fade={{ duration: 400 }}
						src={activeContent.video}
						frameborder="0"
						allow="autoplay; picture-in-picture"
						allowfullscreen
						class="w-full p-0 m-0 h-48 mt-4 px-4"
					/>
					<div>
						<p
							class="text-justify p-4 pb-0 mb-0 text-sm max-h-44"
							in:fade={{ duration: 2500 }}
							out:fade={{ duration: 400 }}
						>
							{activeContent.text}
						</p>
					</div>
				{/if}
			</div>
			<div class=" w-full h-full border-b-4 border-l-4 border-black" />
			<div
				class="z-10 t-0 l-0 h-full absolute overlay grid grid-cols-1 place-items-center"
			>
				<div class="motto">
					<div class="grid grid-cols-1 place-items-left h-full pb-6">
						<a class="content-link" on:click={activate("tide")}>TIDE AD</a>
						<a class="content-link" on:click={activate("got2be")}>Göt2b</a>
						<a class="content-link">OLAY</a>
						<a class="content-link">NEOM</a>
						<a class="content-link">VERIZON</a>
						<a class="content-link">BELLAGIO</a>
						<a class="content-link">NEOM BILLBOARD</a>
						<a class="content-link">DONATE LIFE</a>
						<a class="content-link">METAVERSE</a>
					</div>
				</div>
			</div>
			<div class=" w-full h-full" />
			<div class=" w-full h-full" />
		</div>
		<div class="row-span-3 grid grid-cols-5 place-items-center w-full mb-20">
			<div class=" w-full h-full" />
			<div class=" w-full h-full" />
			<div class="  w-full h-full border-r-4 border-black relative">
				<div class="arrow" />
			</div>
			<div class="  w-full h-full" />
			<div class="  w-full h-full" />
		</div>
	</div>
</div>

<style lang="postcss">
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
		font-size: 11rem;
		letter-spacing: 0.1em;
		@apply row-span-5  w-full h-full ml-80;
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
</style>
