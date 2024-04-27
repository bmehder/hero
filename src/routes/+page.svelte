<script>
	import '@picocss/pico'
	import '$lib/app.css'
	import { backgoundImage, lorem32 } from '$lib/utils.js'
	import Hero from '$lib/Hero.svelte'
	import Controls from '$lib/Controls.svelte'

	let isOpen = false

	const handleClick = () => (isOpen = !isOpen)

	let app = {
		height: 100,
		opacity: 0.5,
		backgoundImage,
		backgroundPositionX: 'center',
		backgroundPositionY: 'center',
		backgoundSize: 100,
		textPositionX: 'center',
		textPositionY: 'center',
		textShadow: 0.125,
		gap: 0.5,
	}

	let mainHeading = {
		color: '#ffffff',
		text: 'Lorem Ipsum Dolor',
		font: 'Poppins',
		fontSize: 4,
		fontWeight: 600,
		lineHeight: 1,
		letterSpacing: 0,
		isUppercase: false,
		isItalic: false,
	}

	let leadHeading = {
		color: '#ffffff',
		text: 'Lorem Ipsum',
		font: 'Poppins',
		fontSize: 1.5,
		fontWeight: 300,
		lineHeight: 1,
		letterSpacing: 3,
		isUppercase: true,
		isItalic: false,
	}

	let content = {
		color: '#ffffff',
		text: lorem32,
		font: 'Poppins',
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
		color: '#323232',
		paddingBlock: 0.5,
		paddingInline: 1,
		font: 'Poppins',
		fontSize: 1,
		fontWeight: 500,
		lineHeight: 1.5,
		letterSpacing: 0,
		isUppercase: false,
	}
</script>

<div class="hero-app">
	<Hero
		bind:app
		bind:content
		bind:leadHeading
		bind:mainHeading
		bind:button
		on:click={handleClick}
	/>

	<Controls
		bind:app
		bind:content
		bind:leadHeading
		bind:mainHeading
		bind:button
		{isOpen}
	/>
</div>

<style>
	.hero-app {
		display: grid;
		gap: 2rem;
	}
</style>
