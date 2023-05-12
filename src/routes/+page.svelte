<script>
	import Flower from '$lib/Flower.svelte';

	export let data;
	const flowers = data.flowers;
</script>

<svg width="1000" height="1000">
	{#each flowers as flower, idx}
		<g
			transform="translate({25 + Math.floor(idx / 10) * 50}, 
								 {25 +(idx % 10) * 50})"
		>
			<Flower {flower} />
		</g>
	{/each}
</svg>
