<script lang="ts">
	import Nav from '$lib/Nav.svelte';
	import '../app.scss';
</script>





<main>
	<Nav/>
	<slot  />

</main>

<style lang="scss">
main {
		padding: 1.5em;
		margin: 0 auto;
	}

</style>


