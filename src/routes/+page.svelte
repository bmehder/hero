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
    isShowOutline: false,
	}

	let mainHeading = {
    marginBlockStart: 0,
    marginBlockEnd: 0,
    marginInline: 0,
    paddingBlock: 0.5,
		paddingInline: 1,
    backgroundColor: '#ffffff',
    isBackgroundTransparent: true,
		color: '#ffffff',
		text: 'Lorem Ipsum Dolor',
		font: 'Poppins',
		fontSize: 4,
		fontWeight: 600,
		lineHeight: 1,
		letterSpacing: 0,
    borderRadius: 0,
		isUppercase: false,
		isItalic: false,
    isShow: true
	}

	let leadHeading = {
    marginBlockStart: 0,
    marginBlockEnd: 0,
    marginInline: 0,
    paddingBlock: 0.5,
		paddingInline: 1,
		backgroundColor: '#ffffff',
    isBackgroundTransparent: true,
    color: '#ffffff',
		text: 'Lorem Ipsum',
		font: 'Poppins',
		fontSize: 1.5,
		fontWeight: 300,
		lineHeight: 1,
		letterSpacing: 3,
    borderRadius: 0,
		isUppercase: true,
		isItalic: false,
    isShow: true
	}

	let content = {
		text: lorem32,
    backgroundColor: '#ffffff',
    isBackgroundTransparent: true,
		color: '#ffffff',
    marginBlockStart: 0,
    marginBlockEnd: 0,
    marginInline: 0,
    paddingBlock: 0.5,
		paddingInline: 1,
		font: 'Poppins',
		fontSize: 1,
		fontWeight: 500,
		lineHeight: 1.5,
		letterSpacing: 0,
    borderRadius: 0,
		isUppercase: false,
		isItalic: false,
    isShow: true
	}

	let button = {
		text: 'Apply Now',
    href: 'https://example.com/',
		backgroundColor: '#ffffff',
    isBackgroundTransparent: false,
		color: '#323232',
    marginBlockStart: 1,
    marginBlockEnd: 1,
    marginInline: 1,
		paddingBlock: 0.5,
		paddingInline: 1,
		font: 'Poppins',
		fontSize: 1,
		fontWeight: 500,
		lineHeight: 1.5,
		letterSpacing: 0,
    borderWidth: 0,
    borderColor: '#ffffff',
    borderRadius: 0,
		isUppercase: false,
    isShow: true,
    isOpenBlank: false,
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
