<script>
  import { fade } from 'svelte/transition';
</script>

<div in:fade={{delay: 100}} out:fade={{duration: 0}}>
	<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
		<path
			fill="currentColor"
			d="M10 20a10 10 0 0 1 0-20a10 10 0 1 1 0 20m-2-5l9-8.5L15.5 5L8 12L4.5 8.5L3 10z"
		/>
	</svg>
	<span>Copied!</span>
</div>

<style>
	div {
		display: flex;
		justify-content: center;
    gap: 0.5rem;
	}

	svg {
		width: 1rem;
	}
</style>
