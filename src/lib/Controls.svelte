<script>
	import Copied from '$lib/Copied.svelte'

	export let app
	export let mainHeading
	export let leadHeading
	export let content
	export let button
	export let isOpen

	let isShowCopied = false

	const copyHero = () => {
		navigator.clipboard.writeText(
			`<style>
				.app {
					display: grid;
					gap: 2rem;
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
			</style>` + document.querySelector('.hero').outerHTML
		)

		isShowCopied = true

		setTimeout(() => (isShowCopied = false), 2000)
	}
</script>

<div class="controls" class:isOpen>
	<button class="secondary" on:click={copyHero} disabled={isShowCopied}>
		{#if isShowCopied}
			<Copied />
		{:else}
			Copy HTML
		{/if}
	</button>

	<!-- Background -->
	<details>
		<summary>Background</summary>

		<div class="input-group">
			<label for="background-image">Background Image URL</label>
			<input id="background-image" bind:value={app.backgoundImage} />
		</div>

		<div class="input-group">
			<label for="min-height">Minimum Height</label>
			<input type="range" id="min-height" min="0" max="100" bind:value={app.height} />
		</div>

		<div class="input-group">
			<label for="gap">Spacing: {app.gap}rem</label>
			<input type="range" id="gap" bind:value={app.gap} min="0" max="5" step="0.25" />
		</div>

		<div class="input-group">
			<label for="opacity">Overlay Opacity: {app.opacity}</label>
			<input
				type="range"
				id="opacity"
				bind:value={app.opacity}
				min="0"
				max="1"
				step="0.1"
			/>
		</div>

		<div class="input-group">
			<label for="background-position-x">Background Position X</label>
			<select id="background-position-x" bind:value={app.backgroundPositionX}>
				<option>left</option>
				<option>center</option>
				<option>right</option>
			</select>

			<label for="background-position-y">Background Position Y</label>
			<select id="background-position-y" bind:value={app.backgroundPositionY}>
				<option>top</option>
				<option>center</option>
				<option>bottom</option>
			</select>
		</div>
	</details>

	<!-- Lead -->
	<details>
		<summary>Lead</summary>

		<div class="input-group">
			<label for="lead-heading-show"> Show Lead Heading? </label><input
				type="checkbox"
				id="lead-heading-show"
				bind:checked={leadHeading.isShow}
			/>
		</div>

		<div class="input-group">
			<label for="lead-heading-margin-block-start">
				Lead Heading Margin Block Start: {leadHeading.marginBlockStart}rem
			</label>
			<input
				type="range"
				id="lead-heading-margin-block-start"
				bind:value={leadHeading.marginBlockStart}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>
		
		<div class="input-group">
			<label for="lead-heading-margin-block-end">
				Lead Heading Margin Block End: {leadHeading.marginBlockEnd}rem
			</label>
			<input
				type="range"
				id="lead-heading-margin-block-end"
				bind:value={leadHeading.marginBlockEnd}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>
		
		<div class="input-group">
			<label for="lead-heading-margin-inline">
				Lead Heading Margin Inline: {leadHeading.marginInline}rem
			</label>
			<input
				type="range"
				id="lead-heading-margin-inline"
				bind:value={leadHeading.marginInline}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="lead-heading-padding-block">
				Lead Heading Padding Block: {leadHeading.paddingBlock}rem
			</label>
			<input
				type="range"
				id="lead-heading-padding-block"
				bind:value={leadHeading.paddingBlock}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="lead-heading-padding-inline">
				Lead Heading Padding Inline: {leadHeading.paddingInline}rem
			</label>
			<input
				type="range"
				id="lead-heading-padding-inline"
				bind:value={leadHeading.paddingInline}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="lead-heading">Lead Text</label>
			<input type="text" id="lead-heading" bind:value={leadHeading.text} />
		</div>

		<div class="input-group">
			<label for="font">Font Family</label>
			<select id="font" bind:value={leadHeading.font}>
				<option>Poppins</option>
				<option>Montserrat</option>
				<option>Oswald</option>
			</select>
		</div>

		<div class="input-group two-col">
			<label for="lead-heading-uppercase"> Lead Heading Uppercase? </label>
			<input
				type="checkbox"
				id="lead-heading-uppercase"
				bind:checked={leadHeading.isUppercase}
			/>
		</div>

		<div class="input-group">
			<label for="lead-Heading-italic"> Lead Heading Italic? </label>
			<input
				type="checkbox"
				id="lead-heading-italic"
				bind:checked={leadHeading.isItalic}
			/>
		</div>

		<div class="input-group">
			<label for="lead-heading-font-size">
				Lead Heading Font Size: {leadHeading.fontSize}rem
			</label>
			<input
				type="range"
				id="lead-heading-font-size"
				bind:value={leadHeading.fontSize}
				min="0.5"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="lead-heading-line-height">
				Lead Heading Line Height: {leadHeading.lineHeight}
			</label>
			<input
				type="range"
				id="lead-heading-line-height"
				bind:value={leadHeading.lineHeight}
				min="0.5"
				max="5"
				step="0.25"
			/>
		</div>

		<div class="input-group">
			<label for="lead-heading-font-weight">
				Lead Heading Font Weight: {leadHeading.fontWeight}
			</label>
			<input
				type="range"
				id="lead-heading-font-weight"
				bind:value={leadHeading.fontWeight}
				min="100"
				max="900"
				step="100"
			/>
		</div>

		<div class="input-group">
			<label for="lead-heading-letter-spacing">
				Lead Heading Letter Spacing: {leadHeading.letterSpacing}px
			</label>
			<input
				type="range"
				id="lead-heading-letter-spacing"
				bind:value={leadHeading.letterSpacing}
				min="0"
				max="5"
			/>
		</div>

		<div class="input-group">
			<label for="lead-heading-color">
				Lead Heading Background Color: {leadHeading.backgroundColor}
			</label>
			<input
				type="color"
				id="lead-heading-color"
				bind:value={leadHeading.backgroundColor}
			/>
		</div>

		<div class="input-group">
			<label for="lead-heading-color">
				Lead Heading Color: {leadHeading.color}
			</label>
			<input type="color" id="lead-heading-color" bind:value={leadHeading.color} />
		</div>

		<div class="input-group">
			<label for="lead-heading-border-radius">
				Lead Heading Border Radius: {leadHeading.borderRadius}px
			</label>
			<input
				type="number"
				id="lead-heading-border-radius"
				bind:value={leadHeading.borderRadius}
				min="0"
				max="100"
			/>
		</div>

		<div class="input-group">
			<label for="lead-heading-background-transparent">
				Lead Heading Background Transparent?
			</label><input
				type="checkbox"
				id="lead-heading-background-transparent"
				bind:checked={leadHeading.isBackgroundTransparent}
			/>
		</div>
	</details>

	<!-- Main -->
	<details>
		<summary>Main</summary>

		<div class="input-group">
			<label for="main-heading-show"> Show Main Heading? </label><input
				type="checkbox"
				id="main-heading-show"
				bind:checked={mainHeading.isShow}
			/>
		</div>

		<div class="input-group">
			<label for="main-heading-margin-block-start">
				Main Heading Margin Block Start: {mainHeading.marginBlockStart}rem
			</label>
			<input
				type="range"
				id="content-margin-block-start"
				bind:value={mainHeading.marginBlockStart}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>
		
		<div class="input-group">
			<label for="main-heading-margin-block-end">
				Main Heading Margin Block End: {mainHeading.marginBlockEnd}rem
			</label>
			<input
				type="range"
				id="main-heading-margin-block-end"
				bind:value={mainHeading.marginBlockEnd}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>
		
		<div class="input-group">
			<label for="main-heading-margin-inline">
				Main Heading Margin Inline: {mainHeading.marginInline}rem
			</label>
			<input
				type="range"
				id="main-heading-margin-inline"
				bind:value={mainHeading.marginInline}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="main-heading-padding-block">
				Main Heading Padding Block: {mainHeading.paddingBlock}rem
			</label>
			<input
				type="range"
				id="main-heading-padding-block"
				bind:value={mainHeading.paddingBlock}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="main-heading-padding-inline">
				Main Heading Padding Inline: {mainHeading.paddingInline}rem
			</label>
			<input
				type="range"
				id="main-heading-padding-inline"
				bind:value={mainHeading.paddingInline}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="main-heading">Main Text</label>
			<input type="text" id="main-heading" bind:value={mainHeading.text} />
		</div>

		<div class="input-group">
			<label for="font">Font Family</label>
			<select id="font" bind:value={mainHeading.font}>
				<option>Poppins</option>
				<option>Montserrat</option>
				<option>Oswald</option>
			</select>
		</div>

		<div class="input-group">
			<label for="main-heading-uppercase"> Main Heading Uppercase? </label><input
				type="checkbox"
				id="main-heading-uppercase"
				bind:checked={mainHeading.isUppercase}
			/>
		</div>

		<div class="input-group">
			<label for="mainHeading-italic"> Main Heading Italic? </label>
			<input
				type="checkbox"
				id="main-heading-italic"
				bind:checked={mainHeading.isItalic}
			/>
		</div>

		<div class="input-group">
			<label for="main-heading-font-size">
				Main Heading Font Size: {mainHeading.fontSize}rem
			</label>
			<input
				type="range"
				id="main-heading-font-size"
				bind:value={mainHeading.fontSize}
				min="0.5"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="main-heading-line-height">
				Main Heading Line Height: {mainHeading.lineHeight}
			</label>
			<input
				type="range"
				id="main-heading-line-height"
				bind:value={mainHeading.lineHeight}
				min="0.5"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="main-heading-font-weight">
				Main Heading Font Weight: {mainHeading.fontWeight}
			</label>
			<input
				type="range"
				id="main-heading-font-weight"
				bind:value={mainHeading.fontWeight}
				min="100"
				max="900"
				step="100"
			/>
		</div>

		<div class="input-group">
			<label for="main-heading-letter-spacing">
				Main Heading Letter Spacing: {mainHeading.letterSpacing}px
			</label>
			<input
				type="range"
				id="main-heading-letter-spacing"
				bind:value={mainHeading.letterSpacing}
				min="0"
				max="5"
			/>
		</div>

		<div class="input-group">
			<label for="main-heading-color">
				Main Heading Background Color: {mainHeading.backgroundColor}
			</label>
			<input
				type="color"
				id="main-heading-color"
				bind:value={mainHeading.backgroundColor}
			/>
		</div>

		<div class="input-group">
			<label for="main-heading-color">
				Main Heading Color: {mainHeading.color}
			</label>
			<input type="color" id="main-heading-color" bind:value={mainHeading.color} />
		</div>

		<div class="input-group">
			<label for="main-heading-border-radius">
				Main Heading Border Radius: {mainHeading.borderRadius}px
			</label>
			<input
				type="number"
				id="main-heading-border-radius"
				bind:value={mainHeading.borderRadius}
				min="0"
				max="100"
			/>
		</div>

		<div class="input-group">
			<label for="main-heading-background-transparent">
				Main Heading Background Transparent?
			</label><input
				type="checkbox"
				id="main-heading-background-transparent"
				bind:checked={mainHeading.isBackgroundTransparent}
			/>
		</div>
	</details>

	<!-- Content -->
	<details>
		<summary>Content</summary>

		<div class="input-group">
			<label for="content-show"> Show Content? </label><input
				type="checkbox"
				id="content-show"
				bind:checked={content.isShow}
			/>
		</div>

		<div class="input-group">
			<label for="content-margin-block-start">
				Content Margin Block Start: {content.marginBlockStart}rem
			</label>
			<input
				type="range"
				id="content-margin-block-start"
				bind:value={content.marginBlockStart}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>
		
		<div class="input-group">
			<label for="content-margin-block-end">
				Content Margin Block End: {content.marginBlockEnd}rem
			</label>
			<input
				type="range"
				id="content-margin-block-end"
				bind:value={content.marginBlockEnd}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>
		
		<div class="input-group">
			<label for="content-margin-inline">
				Content Margin Inline: {content.marginInline}rem
			</label>
			<input
				type="range"
				id="content-margin-inline"
				bind:value={content.marginInline}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="content-padding-block">
				Content Padding Block: {content.paddingBlock}rem
			</label>
			<input
				type="range"
				id="content-padding-block"
				bind:value={content.paddingBlock}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="content-padding-inline">
				Content Padding Inline: {content.paddingInline}rem
			</label>
			<input
				type="range"
				id="content-padding-inline"
				bind:value={content.paddingInline}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="content">Content Text</label>
			<textarea type="text" id="content" bind:value={content.text} rows="4"></textarea>
		</div>

		<div class="input-group">
			<label for="font">Font Family</label>
			<select id="font" bind:value={content.font}>
				<option>Poppins</option>
				<option>Montserrat</option>
				<option>Oswald</option>
			</select>
		</div>

		<div class="input-group">
			<label for="content-uppercase"> Content Uppercase? </label><input
				type="checkbox"
				id="content-uppercase"
				bind:checked={content.isUppercase}
			/>
		</div>

		<div class="input-group">
			<label for="content-italic"> Content Italic? </label><input
				type="checkbox"
				id="content-italic"
				bind:checked={content.isItalic}
			/>
		</div>

		<div class="input-group">
			<label for="content-font-size">
				Content Font Size: {content.fontSize}rem
			</label>
			<input
				type="range"
				id="content-font-size"
				bind:value={content.fontSize}
				min="0.5"
				max="3"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="content-line-height">
				Content Line Height: {content.lineHeight}
			</label>
			<input
				type="range"
				id="content-line-height"
				bind:value={content.lineHeight}
				min="0.5"
				max="3"
				step="0.25"
			/>
		</div>

		<div class="input-group">
			<label for="content-font-weight">
				Content Font Weight: {content.fontWeight}
			</label>
			<input
				type="range"
				id="content-font-weight"
				bind:value={content.fontWeight}
				min="100"
				max="900"
				step="100"
			/>
		</div>

		<div class="input-group">
			<label for="content-letter-spacing">
				Content Letter Spacing: {content.letterSpacing}px
			</label>
			<input
				type="range"
				id="content-letter-spacing"
				bind:value={content.letterSpacing}
				min="0"
				max="5"
			/>
		</div>

		<div class="input-group">
			<label for="content-color">
				Content Color: {content.color}
			</label>
			<input type="color" id="content-color" bind:value={content.color} />
		</div>

		<div class="input-group">
			<label for="content-background-color">
				Content Background Color: {content.backgroundColor}
			</label>
			<input
				type="color"
				id="content-background-color"
				bind:value={content.backgroundColor}
			/>
		</div>

		<div class="input-group">
			<label for="content-border-radius">
				Content Border Radius: {content.borderRadius}px
			</label>
			<input
				type="number"
				id="content-border-radius"
				bind:value={content.borderRadius}
				min="0"
				max="100"
			/>
		</div>

		<div class="input-group">
			<label for="content-background-transparent">
				Content Background Transparent?
			</label><input
				type="checkbox"
				id="content-background-transparent"
				bind:checked={content.isBackgroundTransparent}
			/>
		</div>
	</details>

	<!-- Button -->
	<details>
		<summary>Button</summary>

		<div class="input-group">
			<label for="button-show"> Show Button? </label><input
				type="checkbox"
				id="button-show"
				bind:checked={button.isShow}
			/>
		</div>

		<div class="input-group">
			<label for="button-href">Button URL</label>
			<input id="button-href" bind:value={button.href} />
		</div>

		<div class="input-group">
			<label for="button-new-window"> Open in New Window? </label><input
				type="checkbox"
				id="button-new-window"
				bind:checked={button.isOpenBlank}
			/>
		</div>

		<div class="input-group">
			<label for="button-margin-block-start">
				Button Margin Block Start: {button.marginBlockStart}rem
			</label>
			<input
				type="range"
				id="button-margin-block-start"
				bind:value={button.marginBlockStart}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>
		
		<div class="input-group">
			<label for="button-margin-block-end">
				Button Margin Block End: {button.marginBlockEnd}rem
			</label>
			<input
				type="range"
				id="button-margin-block-end"
				bind:value={button.marginBlockEnd}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>
		
		<div class="input-group">
			<label for="button-margin-inline">
				Button Margin Inline: {button.marginInline}rem
			</label>
			<input
				type="range"
				id="button-margin-inline"
				bind:value={button.marginInline}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>
		
		<div class="input-group">
			<label for="button-padding-block">
				Button Padding Block: {button.paddingBlock}rem
			</label>
			<input
				type="range"
				id="button-padding-block"
				bind:value={button.paddingBlock}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="button-padding-inline">
				Button Padding Inline: {button.paddingInline}rem
			</label>
			<input
				type="range"
				id="button-padding-inline"
				bind:value={button.paddingInline}
				min="0"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="button-text">Button Text</label>
			<input type="text" id="button-text" bind:value={button.text} />
		</div>

		<div class="input-group">
			<label for="font">Font Family</label>
			<select id="font" bind:value={button.font}>
				<option>Poppins</option>
				<option>Montserrat</option>
				<option>Oswald</option>
			</select>
		</div>

		<div class="input-group">
			<label for="button-uppercase"> Button Uppercase? </label>
			<input type="checkbox" id="button-uppercase" bind:checked={button.isUppercase} />
		</div>

		<div class="input-group">
			<label for="button-font-size">
				Button Font Size: {button.fontSize}rem
			</label>
			<input
				type="range"
				id="button-font-size"
				bind:value={button.fontSize}
				min="0.5"
				max="5"
				step="0.5"
			/>
		</div>

		<div class="input-group">
			<label for="button-line-height">
				Button Line Height: {button.lineHeight}
			</label>
			<input
				type="range"
				id="button-line-height"
				bind:value={button.lineHeight}
				min="0.5"
				max="5"
				step="0.25"
			/>
		</div>

		<div class="input-group">
			<label for="button-font-weight">
				Button Font Weight: {button.fontWeight}
			</label>
			<input
				type="range"
				id="button-font-weight"
				bind:value={button.fontWeight}
				min="100"
				max="900"
				step="100"
			/>
		</div>

		<div class="input-group">
			<label for="button-letter-spacing">
				Button Letter Spacing: {button.letterSpacing}px
			</label>
			<input
				type="range"
				id="button-letter-spacing"
				bind:value={button.letterSpacing}
				min="0"
				max="5"
			/>
		</div>
	
		<div class="input-group">
			<label for="button-border-width">
				Button Border Width: {button.borderWidth}px
			</label>
			<input
				type="number"
				id="button-border-width"
				bind:value={button.borderWidth}
				min="0"
				max="20"
			/>
		</div>

		<div class="input-group">
			<label for="button-border-color">
				Button Border Color: {button.borderColor}
			</label>
			<input
				type="color"
				id="button-border-color"
				bind:value={button.borderColor}
			/>
		</div>
		
		<div class="input-group">
			<label for="button-border-radius">
				Button Border Radius: {button.borderRadius}px
			</label>
			<input
				type="number"
				id="button-border-radius"
				bind:value={button.borderRadius}
				min="0"
				max="100"
			/>
		</div>

		<div class="input-group">
			<label for="button-background-color">
				Button Background Color: {button.backgroundColor}
			</label>
			<input
				type="color"
				id="button-background-color"
				bind:value={button.backgroundColor}
			/>
		</div>

		<div class="input-group">
			<label for="button-color">
				Button Color: {button.color}
			</label>
			<input type="color" id="button-color" bind:value={button.color} />
		</div>

		<div class="input-group">
			<label for="button-background-transparent">
				Button Background Transparent?
			</label><input
				type="checkbox"
				id="button-background-transparent"
				bind:checked={button.isBackgroundTransparent}
			/>
		</div>
	</details>

	<!-- Text -->
	<details>
		<summary>Text</summary>

		<div class="input-group">
			<label for="text-position-x">Text Position X</label>
			<select id="text-position-x" bind:value={app.textPositionX}>
				<option value="start">left</option>
				<option value="center">center</option>
				<option value="end">right</option>
			</select>

			<label for="text-position-y">Text Position Y</label>
			<select id="text-position-y" bind:value={app.textPositionY}>
				<option value="start">top</option>
				<option value="center">center</option>
				<option value="end">bottom</option>
			</select>
		</div>

		<div class="input-group">
			<label for="text-shadow">Text Shadow: {app.textShadow}rem</label>
			<input
				type="range"
				id="text-shadow"
				bind:value={app.textShadow}
				min="0"
				max="1"
				step="0.005"
			/>
		</div>
	</details>
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

	.controls details > * + * {
		margin-block-start: 2rem;
	}

	details[open] {
		padding-block-end: 2rem;
		border-bottom: 2px solid;
	}

	.isOpen {
		right: 0;
	}

	input:not([type='color']),
	textarea,
	select {
		padding: 0.5rem;
		font: inherit;
	}
</style>
