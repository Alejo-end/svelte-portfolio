<script>
	import Board from '$lib/Board.svelte';
	import D3 from '$lib/D3.svelte';


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
	<div class="board">
	<img src="static/biem.svg" alt="logo"/>

	</div>

</main>

<style lang="scss">
	main{
		display: flex;
	}
	.board{
		border: 5px solid #333333;
		align-items: center;
		max-width: min-content;
	}
	.btn {
        display: inline-block;
        font-size: 1em;
        background: #333333;
        padding: 10px 20px;
        text-transform: uppercase;
        text-decoration: none;
        font-weight: 500;
        margin-top: 10px;
        color: #f7f7f7;
        letter-spacing: 2px;
        transition: 0.2s;
        cursor: pointer;
    &:hover {
        letter-spacing: 5px;
        animation: colorRotate 2s linear 0s infinite;
        box-shadow: 5px 5px #333333;
    	}   
	}
	.link-a{
        text-decoration: none;
        color: white;
}
</style>
	



