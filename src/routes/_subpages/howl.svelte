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
						HOWL
					</p>
				</div>
			</div>
		</div>
		<div class="center">
			<Sidebar color="black" />
			<div
				class=" w-full h-full grid grid-cols-1 place-items-center sm:text-xl md:text-3xl lg:text-4xl xl:text-5xl text-right all-round-gothic-book-oblique weight"
			>
				<div>The most</div>
				<div>pressed</div>
				<div>button</div>
				<div>in the</div>
				<div>world is</div>
				<div>"skip ad"</div>
			</div>
			<div
				class=" w-full h-full border-b-4 border-l-4 border-black"
			/>
			<div
				class="z-10 t-0 l-0 h-full absolute overlay grid grid-cols-1 place-items-center"
			>
				<div class="content">
					<div
						class="grid grid-cols-1 place-content-evenly h-full pb-0 pl-6 all-round-gothic-book-oblique"
					>
						<p>
							Most of the time they deserve to be skipped.
						</p>
						<p>
							Because they’re bad, boring, they’re
							just…average.
						</p>
						<p>
							Average is a joy killer. Average is a waste of
							everyone’s time.
						</p>
						<p>
							We’re here with a purpose. To give ideas that
							matter, the ones that people love and engage,
							a bigger chance to exist. That’s why we’re not
							only an ad agency, we’re a production house
							too.
						</p>
						We’re small, faster and more efficient.<br />
						We’re project driven. And we hire accordingly.
						<br />
						We’re here to unleash the kind of work people cannot
						ignore. <br /> We’re here for the joy of doing
						what we love. <br /> We’re here for shorter
						calls and longer relationships. <br /> We want
						everyone involved to be happy. <br /><br />
						<p class="howling font-extrabold">
							And occasionally howling.
						</p>
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
		@apply text-justify  w-full h-full flex flex-col justify-end font-bold pr-6 md:pr-8 lg:pr-20;
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
	.weight {
		font-weight: 100;
	}
	@media (max-width: 1300px) {
		.content {
			font-size: 1rem;
		}
	}
	@media (max-width: 1250px) {
		.content {
			font-size: 0.9rem;
		}
	}
	@media (max-width: 1024px) {
		.content {
			font-size: 0.9rem;
		}
	}
	@media (max-width: 800px) {
		.content {
			font-size: 0.7rem;
		}
	}
	@media (max-width: 540px) {
		.content {
			font-size: 0.6rem;
		}
	}
	@media (max-width: 1024px) {
		.arrow {
			width: 25px;
			height: 25px;
		}
	}
	.howling {
		font-weight: bold;
	}
</style>
