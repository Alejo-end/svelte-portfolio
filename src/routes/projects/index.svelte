<script>
	import Slides from '$lib/Slides.svelte';
	import Board from '$lib/Board.svelte';




</script>

<main>
	<Board width="48em">
		<h1>
			Contact
		</h1>
		
		<p>
			Feel free to contact me in any of these sites:
		</p>
		<div class="buttons">
			<div class="btn"><a href="https://pa.linkedin.com/in/alejo-end" class="link-a">Linkedin</a></div> 
			<br/>
			<div class="btn"><a href="https://github.com/Alejo-end" class="link-a">GitHub</a></div>
			<br/>
			<div class="btn"><a href="alejandroe.deleon@gmail.com" class="link-a">Email</a></div>
		</div>
	</Board>
	<Slides/>

	
</main>

<style lang="scss">
		main{
		display: flex;
	}
</style>

