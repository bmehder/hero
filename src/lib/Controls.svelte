<script>
	import { stylesAsString } from '$lib/utils.js'
	import Copied from '$lib/Copied.svelte'
	import Background from '$lib/Background.svelte'
	import MainHeading from '$lib/MainHeading.svelte'
	import LeadHeading from '$lib/LeadHeading.svelte'
	import Content from '$lib/Content.svelte'
	import Button from '$lib/Button.svelte'
	import Text from '$lib/Text.svelte'

	export let app
	export let mainHeading
	export let leadHeading
	export let content
	export let button
	export let isOpen

	let isShowCopied = false

	const copyHeroHTML = () => {
		navigator.clipboard.writeText(
			stylesAsString + document.querySelector('.hero').outerHTML
		)

		isShowCopied = true

		setTimeout(() => (isShowCopied = false), 2000)
	}
</script>

<div class="controls" class:isOpen>
	<button class="secondary" on:click={copyHeroHTML} disabled={isShowCopied}>
		{#if isShowCopied}
			<Copied />
		{:else}
			Copy HTML
		{/if}
	</button>

	<div class="show-outline">
		<label for="show-outline"> Show Outline (dev)? </label><input
			type="checkbox"
			id="show-outline"
			bind:checked={app.isShowOutline}
		/>
	</div>

	<Background bind:app />

	<LeadHeading bind:leadHeading />

	<MainHeading bind:mainHeading />

	<Content bind:content />

	<Button bind:button />

	<Text bind:app />
</div>

<style>
	.controls {
		width: 24rem;
		max-height: 100dvh;
		position: absolute;
		display: grid;
		gap: 2rem;
		right: -100%;
		z-index: 1;
		padding: 2rem;
		overflow-y: scroll;
		background-color: var(--pico-background-color);
		border-bottom-left-radius: 0.5rem;
		box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
		transition: right 300ms ease-in-out;
	}

	.show-outline {
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 0.5rem;
	}

	.isOpen {
		right: 0;
	}
</style>
