<script>
	import { quintOut } from 'svelte/easing';
	import { fade, draw, fly } from 'svelte/transition';
	import { letteraline, letterdline } from '../utils/shape.js';

	let visible = false;
</script>
<label>
	<input type="checkbox" bind:checked={visible}>
	toggle me
</label>

{#if visible}
	<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 110 110">
		<g out:fade="{{duration: 200}}" >
			<path
				in:draw="{{duration: 1000}}"
				style="stroke:#333333; stroke-width: 2.5;"
				d={letterdline}
			/>

			<path
				in:draw="{{duration: 1000}}"
				style="stroke:#333333; stroke-width: 2.5;"
				d={letteraline}
			/>
			<path
				in:draw="{{duration: 1000}}"
				style="stroke:#333333; stroke-width: 2.5;"
				d="M54 4V43"
			/>
			<path
				in:draw="{{duration: 1000}}"
				style="stroke:#333333; stroke-width: 2.5;"
				d="M78 36H47"
			/>
		</g>
	</svg>
{/if}



<style>
	svg {
		width:  31%;
		right: 0em;
		top: 15em;
    	position: fixed;
	}

	path {
		fill: white;
		opacity: 1;
	}

	@media (max-width: 40px) {
		svg {
		width:  50%;
		right: 50%;
		top: 0;
    	position: fixed;
	}
}


</style>