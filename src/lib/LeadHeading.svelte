<script>
  export let leadHeading
</script>

<details>
	<!-- svelte-ignore a11y-no-redundant-roles -->
	<summary role="button" class="secondary">Lead Heading</summary>

	<div>
		<label for="lead-heading-show"> Show Lead Heading? </label><input
			type="checkbox"
			id="lead-heading-show"
			bind:checked={leadHeading.isShow}
		/>
	</div>

	<div>
		<label for="lead-heading">Lead Text</label>
		<input type="text" id="lead-heading" bind:value={leadHeading.text} />
	</div>

	<div>
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

	<div>
		<label for="lead-Heading-italic"> Lead Heading Italic? </label>
		<input type="checkbox" id="lead-heading-italic" bind:checked={leadHeading.isItalic} />
	</div>

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
		<label for="lead-heading-background-transparent">
			Lead Heading Background Transparent?
		</label><input
			type="checkbox"
			id="lead-heading-background-transparent"
			bind:checked={leadHeading.isBackgroundTransparent}
		/>
	</div>

	<div>
		<label for="lead-heading-color">
			Lead Heading Background Color: {leadHeading.backgroundColor}
		</label>
		<input
			type="color"
			id="lead-heading-color"
			bind:value={leadHeading.backgroundColor}
		/>
	</div>

	<div>
		<label for="lead-heading-color">
			Lead Heading Color: {leadHeading.color}
		</label>
		<input type="color" id="lead-heading-color" bind:value={leadHeading.color} />
	</div>

	<div>
		<label for="lead-heading-border-radius">
			Lead Heading Border Radius: {leadHeading.borderRadius}px
		</label>
		<input
			type="range"
			id="lead-heading-border-radius"
			bind:value={leadHeading.borderRadius}
			min="0"
			max="100"
		/>
	</div>
</details>
