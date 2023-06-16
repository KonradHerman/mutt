<script>
	export let color = "white"
	function scrollIntoView({ target }) {
		const el = document.querySelector(
			target.getAttribute("href")
		)
		if (!el) return
		el.scrollIntoView({
			behavior: "smooth",
		})
	}
</script>

<div
	class="  w-full h-full text-right pr-2 md:pr-10 pt-20 flex flex-col gap-10 items-end text-sm md:text-lg text-{color} all-round-gothic"
>
	<a href="#work" on:click|preventDefault={scrollIntoView}
		>Work</a
	>

	<a href="#howl" on:click|preventDefault={scrollIntoView}
		>Howl</a
	>
	<a href="#people" on:click|preventDefault={scrollIntoView}
		>People</a
	>
	<a href="#awards" on:click|preventDefault={scrollIntoView}
		>Awards</a
	>
	<a href="#woof" on:click|preventDefault={scrollIntoView}
		>Woof</a
	>
</div>

<style>
	.weight {
		font-weight: 100;
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

		transition: width 0.3s ease 0s, left 0.3s ease 0s;
		width: 0;
	}
	div.black a:after {
		background: black !important;
	}
	div.white a:after {
		background: white !important;
	}
	a:hover:after {
		width: 100%;
		left: 0;
	}
</style>
