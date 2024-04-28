<script>
	export let mainHeading
</script>

<details>
	<!-- svelte-ignore a11y-no-redundant-roles -->
	<summary role="button" class="secondary">Main Heading</summary>

	<div>
		<label for="main-heading-show"> Show Main Heading? </label><input
			type="checkbox"
			id="main-heading-show"
			bind:checked={mainHeading.isShow}
		/>
	</div>

	<div>
		<label for="main-heading">Main Text</label>
		<input type="text" id="main-heading" bind:value={mainHeading.text} />
	</div>

	<div>
		<label for="font">Font Family</label>
		<select id="font" bind:value={mainHeading.font}>
			<option>Poppins</option>
			<option>Montserrat</option>
			<option>Oswald</option>
		</select>
	</div>

	<div>
		<label for="main-heading-uppercase"> Main Heading Uppercase? </label><input
			type="checkbox"
			id="main-heading-uppercase"
			bind:checked={mainHeading.isUppercase}
		/>
	</div>

	<div>
		<label for="mainHeading-italic"> Main Heading Italic? </label>
		<input type="checkbox" id="main-heading-italic" bind:checked={mainHeading.isItalic} />
	</div>

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
		<label for="main-heading-background-transparent">
			Main Heading Background Transparent?
		</label><input
			type="checkbox"
			id="main-heading-background-transparent"
			bind:checked={mainHeading.isBackgroundTransparent}
		/>
	</div>

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
		<label for="main-heading-color">
			Main Heading Background Color: {mainHeading.backgroundColor}
		</label>
		<input
			type="color"
			id="main-heading-color"
			bind:value={mainHeading.backgroundColor}
		/>
	</div>

	<div>
		<label for="main-heading-color">
			Main Heading Color: {mainHeading.color}
		</label>
		<input type="color" id="main-heading-color" bind:value={mainHeading.color} />
	</div>

	<div>
		<label for="main-heading-border-radius">
			Main Heading Border Radius: {mainHeading.borderRadius}px
		</label>
		<input
			type="range"
			id="main-heading-border-radius"
			bind:value={mainHeading.borderRadius}
			min="0"
			max="100"
		/>
	</div>
</details>
