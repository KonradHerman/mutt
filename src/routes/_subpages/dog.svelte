<script>
	import Sidebar from "../sidebar.svelte"
    let wink = false;
    let src = "SVG_DOGS/Asset 4.svg"
</script>

<div class="wink">
    <img width="20%" alt="logo" {src} on:mouseenter={() => {
        console.log("enter");
            src="SVG_DOGS/Asset 5.svg"
    }}
    on:mouseleave={() => {
        console.log("leave");
            src="SVG_DOGS/Asset 4.svg"
    }}>
</div>

<style lang="postcss">
    .wink{
        @apply w-full h-full grid grid-cols-1 place-items-center;
    }
</style>