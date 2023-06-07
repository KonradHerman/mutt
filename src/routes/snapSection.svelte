<script>
	export let id
</script>

<section {id}>
	<slot>Loading</slot>
</section>

<style scoped>
	section {
		position: relative;
		height: 100vh;
		display: flex;
		justify-content: center;
		align-items: center;
		scroll-snap-align: start;
	}
</style>
