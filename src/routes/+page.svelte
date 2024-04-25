<script>
  import '@picocss/pico'
	import { backgoundImage, lorem32 } from '$lib/utils.js'
	import Hero from '$lib/Hero.svelte'
	import Controls from '$lib/Controls.svelte'

	let app = {
		opacity: 0.5,
		backgoundImage,
		backgroundPositionX: 'center',
		backgroundPositionY: 'center',
		textPositionX: 'center',
		textPositionY: 'center',
		gap: 1,
	}

	let mainHeading = {
		color: '#ffffff',
		text: 'Lorem Ipsum Dolor',
		fontSize: 2,
		fontWeight: 600,
		lineHeight: 1,
		letterSpacing: 0,
		isUppercase: false,
		isItalic: false,
	}

	let leadHeading = {
		color: '#ffffff',
		text: 'Lorem Ipsum',
		fontSize: 2,
		fontWeight: 600,
		lineHeight: 1.5,
		letterSpacing: 0,
		isUppercase: false,
		isItalic: false,
	}

	let content = {
		color: '#ffffff',
		text: lorem32,
		fontSize: 1,
		fontWeight: 500,
		lineHeight: 1.5,
		letterSpacing: 0,
		isUppercase: false,
		isItalic: false,
	}

	let button = {
		text: 'Apply Now',
		backgroundColor: '#ffffff',
		color: '#333333',
		paddingBlock: 0.5,
		paddingInline: 1,
		fontSize: 1,
		fontWeight: 500,
		lineHeight: 1.5,
		letterSpacing: 0,
		isUppercase: false,
	}
</script>

<div class="app">
	<Hero bind:app bind:content bind:leadHeading bind:mainHeading bind:button />

	<main class="container">
		<div class="input-group">
			<label for="background-image">Background Image</label>
			<input bind:value={app.backgoundImage} />
		</div>

		<Controls bind:app bind:content bind:leadHeading bind:mainHeading bind:button />
	</main>
</div>

<style>
	:global(*) {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	.app {
		display: grid;
		gap: 2rem;
		padding-block-end: 2rem; /* Due to REPL console */
	}

	.input-group {
		display: grid;
		gap: 0.5rem;

		& input {
			padding: 0.5rem;
		}
	}

  /* main {
    width: min(100% - 1.5rem, 80%);
    margin-inline: auto;
  } */
</style>
