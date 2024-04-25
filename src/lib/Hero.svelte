<script>
	export let app
	export let content
	export let leadHeading
	export let mainHeading
	export let button
</script>

<section
	class="hero"
	style="
		background-image: url({app.backgoundImage});
		background-position:
			{app.backgroundPositionX} {app.backgroundPositionY};
		box-shadow:
		 inset 0 0 0 1000px rgba(0, 0, 0, {app.opacity});
		color: {content.color};
	">
	<div
		class="hero-items"
		style="
			justify-items: {app.textPositionX};
			align-content: {app.textPositionY};
			gap: {app.gap}rem;
		"
	>
		<h2
			class="lead-heading"
			class:isUppercase={leadHeading.isUppercase}
			class:italic={leadHeading.isItalic}
			style="
				color: {leadHeading.color};
				font-size: {leadHeading.fontSize}rem;
				font-weight: {leadHeading.fontWeight};
				line-height: {leadHeading.lineHeight};
				letter-spacing: {leadHeading.letterSpacing}px;
			"
		>
			{leadHeading.text}
		</h2>
		<h1
			class="main-heading"
			class:isUppercase={mainHeading.isUppercase}
			class:italic={mainHeading.isItalic}
			style="
				color: {mainHeading.color};
				font-size: {mainHeading.fontSize}rem;
				font-weight: {mainHeading.fontWeight};
				line-height: {mainHeading.lineHeight};
				letter-spacing: {mainHeading.letterSpacing}px;
			"
		>
			{mainHeading.text}
		</h1>
		<div
			class="content"
			class:isUppercase={content.isUppercase}
			class:text-align-left={app.textPositionX === 'start'}
			class:text-align-center={app.textPositionX === 'center'}
			class:text-align-right={app.textPositionX === 'end'}
			class:italic={content.isItalic}
			style="
				color: {content.color};
				font-size: {content.fontSize}rem;
				font-weight: {content.fontWeight};
				line-height: {content.lineHeight};
				letter-spacing: {content.letterSpacing}px;
			"
		>
			{content.text}
		</div>
		
		<button
			style="
				background-color: {button.backgroundColor};
				color: {button.color};
				padding-block: {button.paddingBlock}rem;
				padding-inline: {button.paddingInline}rem;
				font-size: {button.fontSize}rem;
				font-weight: {button.fontWeight};
				line-height: {button.lineHeight};
				letter-spacing: {button.letterSpacing}px;
			"
		>
			{button.text}
		</button>
	</div>
</section>

<style>
	.hero {
		min-height: 70dvh;
		padding: 2rem;
		background-size: cover;
	}

	.hero-items {
		min-height: 100%;
		display: grid;
	}

	.main-heading, .lead-heading {
		line-height: 1.1;
	}
	
	.main-heading, .lead-heading, .content {
		text-shadow: 0 0 0.125rem black;
	}

	.content {
		font-weight: 600;
	}
	
	button {
		margin-block-start: 1rem;
		font: inherit;
		border: none;
	}

	.isUppercase {
		text-transform: uppercase;	
	}

	.text-align-left {
		text-align: left;
	}
	
	.text-align-center {
		text-align: center;
	}
	
	.text-align-right {
		text-align: right;
	}

	.italic {
		font-style: italic;
	}
</style>