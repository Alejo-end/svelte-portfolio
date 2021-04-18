<script lang="ts">
	import { hslide } from '../utils/hslide.js';
	
	let slides = [
		{ content: '1', bg: 'blue' },
		{ content: '2', bg: 'red' },
		{ content: '3', bg: 'green' },
		{ content: '4', bg: 'orange' },
	]
	
	let cur = 0;
	
	function changeSlide(slide) {
		cur = slide;
	}
	
	const clamp = (number, min, max) => Math.min(Math.max(number, min), max);
	const transition_args = {
		duration: 200,
	}
	
	function prev() {
		cur = clamp( --cur, 0, slides.length-1 )
	}
	
	function next() {
		cur = clamp( ++cur, 0, slides.length-1 )
	}
	
  const ARROW_LEFT = 37;
	const ARROW_RIGHT = 39;
	function handleShortcut(e) {
        if (e.keyCode === ARROW_LEFT ) {
						prev();
        }
		    if (e.keyCode === ARROW_RIGHT ) {
            next();
        }
    }

</script>

<svelte:window on:keyup={handleShortcut} />

<div class="extra-outer-wrapper">
	<div class="outer-wrapper">
		<div class="inner-wrapper">
			{#each slides as slide, id}
				{#if id === cur}
				<div
						 style="background:{slide.bg}"
						 class="slide"
						 in:hslide={transition_args}
						 out:hslide={transition_args}
				>
					{slide.content}		
				</div>
				{/if}
			{/each}
			<div class="controls">
				<button on:click="{()=>prev()}">
					&#10094;
				</button>
				<button on:click="{()=>next()}">
					&#10095;
				</button>
			</div>
		</div>
	</div>
</div>

<div class="dots">
	{#each slides as slide, i}
		<button on:click={()=>changeSlide(i)} class="dot" class:selected={cur == i}>{i+1}</button>
	{/each}
</div>

<style lang="scss">

	button {
		background: transparent;
		color: #FFF;
		border: none;
		height: 3rem;
		width: 3rem;
        border-radius: 10%;
        margin: auto 15px;
        transition: 0.7s;
        &:hover,
	    &:focus{
		    background: rgba(0,0,0,0.5);
	    }
	}
	
	.dots {
		display: flex;
		align-items: center;
		justify-content: center;
		margin-top: 20px;
	}
	
	.dot {
		width: 5px;
		height: 5px;
		background: #333;
		border-radius: 25%;
        font-size: 0;
		margin: 0.3rem;
		opacity: 0.3;
        &.selected {
		    opacity: 1;
	    }
	}

	.extra-outer-wrapper {
		width: 60%;
		margin: 0 auto;
	}

	.outer-wrapper {
		width: 100%;
		padding: 0 0 60%;
		position: relative;
	}
	
	.inner-wrapper {
		height: 100%;
		width: 100%;
		display: flex;
		position: absolute;
	}
	
	.slide {
		flex: 1 0 auto;
		width: 100%;
		height: 100%;
	    align-items: center;
		justify-content: center;
		display: flex;
		font-weight: bold;
		font-size: 2rem;
		color: white;
        border: 4px solid #333333;
	}
	
	.controls {
		text-align: center;
		display: block;
        & button:first-child {
            position: absolute;
            left: 0;
            top: calc(50% - 3rem);
        }
	
        & button:last-child {
            position: absolute;
            right: 0;
            top: calc(50% - 3rem);
	    }
	}
    
</style>