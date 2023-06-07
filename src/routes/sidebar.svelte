<script>
	export let color = "white" // can be black or white
</script>

<div
	class=" w-full h-full text-right pr-10 pt-20 flex flex-col gap-10 items-end text-lg {color}"
>
	<a href="">Work</a>

	<a href="">People</a>
	<a href="">Howl</a>
	<a href="">Awards</a>
	<a href="">Woof</a>
</div>

<style>
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
		background: black;
	}
	div.white a:after {
		background: white;
	}
	a:hover:after {
		width: 100%;
		left: 0;
	}
</style>
