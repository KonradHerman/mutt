
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
