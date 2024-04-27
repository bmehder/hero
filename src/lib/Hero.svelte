<script>
	export let app
	export let content
	export let leadHeading
	export let mainHeading
	export let button
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&family=Oswald:wght@200..700&family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<!-- svelte-ignore a11y-click-events-have-key-events -->
<section
	on:click
	class="hero"
	style="
		min-height: {app.height}dvh;
		padding: 2rem;
		background-size: cover;
		background-image: url({app.backgoundImage});
		background-position:
			{app.backgroundPositionX} {app.backgroundPositionY};
		box-shadow:
		 inset 0 0 0 1000px rgba(0, 0, 0, {app.opacity});
		color: {content.color};
	"
>
	<div
		class="hero-items"
		style="
			max-width: 48rem;
			min-height: 100%;
			display: grid;
			justify-items: {app.textPositionX};
			align-content: {app.textPositionY};
			gap: {app.gap}rem;
			margin-inline: auto;
		"
	>
		<h2
			class="lead-heading"
			class:isUppercase={leadHeading.isUppercase}
			class:italic={leadHeading.isItalic}
			class:isShow={leadHeading.isShow}
			style="
				background-color: {leadHeading.isBackgroundTransparent
				? '#ffffff00'
				: leadHeading.backgroundColor};
				color: {leadHeading.color};
				margin-block-start: {leadHeading.marginBlockStart}rem;
				margin-block-end: {leadHeading.marginBlockEnd}rem;
				margin-inline: {leadHeading.marginInline}rem;
				padding-block: {leadHeading.paddingBlock}rem;
				padding-inline: {leadHeading.paddingInline}rem;
				font-family: {leadHeading.font}, sans-serif;
				font-size: {leadHeading.fontSize}rem;
				font-weight: {leadHeading.fontWeight};
				line-height: {leadHeading.lineHeight};
				letter-spacing: {leadHeading.letterSpacing}px;
				text-shadow: 0 0 {app.textShadow}rem black;
				border-radius: {leadHeading.borderRadius}px;
			"
		>
			{leadHeading.text}
		</h2>
		<h1
			class="main-heading"
			class:isUppercase={mainHeading.isUppercase}
			class:italic={mainHeading.isItalic}
			class:isShow={mainHeading.isShow}
			style="
				background-color: {mainHeading.isBackgroundTransparent
				? '#ffffff00'
				: mainHeading.backgroundColor};
				color: {mainHeading.color};
				margin-block-start: {mainHeading.marginBlockStart}rem;
				margin-block-end: {mainHeading.marginBlockEnd}rem;
				margin-inline: {mainHeading.marginInline}rem;
				padding-block: {mainHeading.paddingBlock}rem;
				padding-inline: {mainHeading.paddingInline}rem;
				font-family: {mainHeading.font}, sans-serif;
				font-size: {mainHeading.fontSize}rem;
				font-weight: {mainHeading.fontWeight};
				line-height: {mainHeading.lineHeight};
				letter-spacing: {mainHeading.letterSpacing}px;
				text-shadow: 0 0 {app.textShadow}rem black;
				text-align: center;
				border-radius: {mainHeading.borderRadius}px;
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
			class:isShow={content.isShow}
			style="
				background-color: {content.isBackgroundTransparent
				? '#ffffff00'
				: content.backgroundColor};
				color: {content.color};
				margin-block-start: {content.marginBlockStart}rem;
				margin-block-end: {content.marginBlockEnd}rem;
				margin-inline: {content.marginInline}rem;
				padding-block: {content.paddingBlock}rem;
				padding-inline: {content.paddingInline}rem;
				font-family: {content.font}, sans-serif;
				font-size: {content.fontSize}rem;
				font-weight: {content.fontWeight};
				line-height: {content.lineHeight};
				letter-spacing: {content.letterSpacing}px;
				text-shadow: 0 0 {app.textShadow}rem black;
				border-radius: {content.borderRadius}px;
			"
		>
			{content.text}
		</div>

		<a
			class="button"
			class:isUppercase={button.isUppercase}
			class:isShow={button.isShow}
			style="
				margin-block-start: {button.marginBlockStart}rem;
				margin-block-end: {button.marginBlockEnd}rem;
				margin-inline: {button.marginInline}rem;
				padding-block: {button.paddingBlock}rem;
				padding-inline: {button.paddingInline}rem;
				background-color: {button.isBackgroundTransparent
				? '#ffffff00'
				: button.backgroundColor};
				color: {button.color};
				font-family: {button.font}, sans-serif;
				font-size: {button.fontSize}rem;
				font-weight: {button.fontWeight};
				line-height: {button.lineHeight};
				text-decoration: none;
				letter-spacing: {button.letterSpacing}px;
				border: none;
				outline-style: solid;
				outline-width: {button.borderWidth}px;
				outline-color: {button.borderColor};
				outline-radius: {button.borderRadius}px;
			"
			href={button.href}
			target={button.isOpenBlank ? '_blank' : '_self'}
		>
			{button.text}
		</a>
	</div>
</section>

<style>
	.main-heading, .lead-heading, .content, .button {
		display: none;
	}

	.isShow {
		display: block;
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
