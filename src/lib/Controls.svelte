<script>
	export let app
	export let mainHeading
	export let leadHeading
	export let content
	export let button
</script>

<div class="controls">
	<div class="input-group">
		<label for="background-image">Background Image</label>
		<input bind:value={app.backgoundImage} />
	</div>

	<div class="input-group">
		<label for="main-heading">Main Heading</label>
		<input type="text" id="main-heading" bind:value={mainHeading.text} />
	</div>

	<div class="input-group">
		<label for="lead-heading">Lead Heading</label>
		<input type="text" id="lead-heading" bind:value={leadHeading.text} />
	</div>

	<div class="input-group">
		<label for="content">Content</label>
		<textarea type="text" id="content" bind:value={content.text} rows="4"></textarea>
	</div>

	<div class="input-group">
		<label for="button-text">Button Text</label>
		<input type="text" id="button-text" bind:value={button.text} />
	</div>

	<div class="input-group">
		<label for="background-position">Background Position</label>
		<select id="background-position" bind:value={app.backgroundPositionX}>
			<option>center</option>
			<option>left</option>
			<option>right</option>
		</select>
		<select id="background-position" bind:value={app.backgroundPositionY}>
			<option>center</option>
			<option>top</option>
			<option>bottom</option>
		</select>
	</div>

	<div class="input-group">
		<label for="text-position">Text Position</label>
		<select id="text-position" bind:value={app.textPositionX}>
			<option value="start">left</option>
			<option value="center">center</option>
			<option value="end">right</option>
		</select>
		<select id="text-position" bind:value={app.textPositionY}>
			<option value="start">top</option>
			<option value="center">center</option>
			<option value="end">bottom</option>
		</select>
	</div>

	<div class="input-group">
		<label for="gap">Spacing: {app.gap}rem</label>
		<input type="range" id="gap" bind:value={app.gap} min="0" max="5" step="0.5" />
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

	<div class="input-group two-col">
		<label for="main-heading-uppercase"> Main Heading Uppercase? </label>
		<input
			type="checkbox"
			id="main-heading-uppercase"
			bind:checked={mainHeading.isUppercase}
		/>
	</div>

	<div class="input-group two-col">
		<label for="lead-heading-uppercase"> Lead Heading Uppercase? </label>
		<input
			type="checkbox"
			id="lead-heading-uppercase"
			bind:checked={leadHeading.isUppercase}
		/>
	</div>

	<div class="input-group two-col">
		<label for="content-uppercase"> Content Uppercase? </label>
		<input type="checkbox" id="content-uppercase" bind:checked={content.isUppercase} />
	</div>

	<div class="input-group two-col">
		<label for="mainHeading-italic"> Main Heading Italic? </label>
		<input type="checkbox" id="main-heading-italic" bind:checked={mainHeading.isItalic} />
	</div>

	<div class="input-group two-col">
		<label for="leadHeading-italic"> Lead Heading Italic? </label>
		<input type="checkbox" id="lead-heading-italic" bind:checked={leadHeading.isItalic} />
	</div>

	<div class="input-group two-col">
		<label for="content-italic"> Content Italic? </label>
		<input type="checkbox" id="content-italic" bind:checked={content.isItalic} />
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
			Main Heading Line Height: {mainHeading.lineHeight}em
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
			Lead Heading Line Height: {leadHeading.lineHeight}em
		</label>
		<input
			type="range"
			id="lead-heading-line-height"
			bind:value={leadHeading.lineHeight}
			min="0.5"
			max="5"
			step="0.5"
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
			Content Line Height: {content.lineHeight}em
		</label>
		<input
			type="range"
			id="content-line-height"
			bind:value={content.lineHeight}
			min="0.5"
			max="3"
			step="0.5"
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
			Button Line Height: {button.lineHeight}em
		</label>
		<input
			type="range"
			id="button-line-height"
			bind:value={button.lineHeight}
			min="0.5"
			max="5"
			step="0.5"
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
		<label for="main-heading-color">
			Main Heading Color: {mainHeading.color}
		</label>
		<input type="color" id="main-heading-color" bind:value={mainHeading.color} />
	</div>

	<div class="input-group">
		<label for="lead-heading-color">
			Lead Heading Color: {leadHeading.color}
		</label>
		<input type="color" id="lead-heading-color" bind:value={leadHeading.color} />
	</div>

	<div class="input-group">
		<label for="content-color">
			Content Color: {content.color}
		</label>
		<input type="color" id="content-color" bind:value={content.color} />
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
</div>

<style>
	.controls {
		height: 400px;
		display: grid;
		gap: 2rem;
		overflow-y: scroll;
	}

	.two-col {
		grid-template-columns: repeat(2, 1fr);
	}

	input:not([type='color']),
	textarea,
	select {
		padding: 0.5rem;
		font: inherit;
	}
</style>
