<script>
  import { fade } from 'svelte/transition';
</script>

<div transition:fade>
	<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
		<path
			fill="currentColor"
			d="M10 20a10 10 0 0 1 0-20a10 10 0 1 1 0 20m-2-5l9-8.5L15.5 5L8 12L4.5 8.5L3 10z"
		/>
	</svg>
	<p>Copied!</p>
</div>

<style>
	div {
		position: absolute;
		top: 1rem;
		right: 1rem;
		display: grid;
		justify-items: center;
	}

	svg {
		width: 2rem;
	}
</style>
