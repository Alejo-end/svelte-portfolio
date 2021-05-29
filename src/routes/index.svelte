<script lang="ts">
	import Board from '$lib/Board.svelte';
	import D3 from '$lib/D3.svelte';
import Welcome from '$lib/Welcome.svelte';

</script>

<main>
	<Board>
		<D3/>
		<Welcome/>
	</Board>

</main>

<style lang="scss">
	main {
		margin: 0 auto;
	}

	@media (min-width: 480px) {

	}
</style>
