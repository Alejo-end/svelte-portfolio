<script lang="ts">
	import Counter from '$lib/Counter.svelte';
	import Board from '$lib/Board.svelte';
	import D3 from '$lib/D3.svelte';

</script>

<main>
	<Board/>
	<D3/>

</main>

<style lang="scss">
	main {
		margin: 0 auto;
	}

	@media (min-width: 480px) {

	}
</style>
