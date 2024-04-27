<script>
  export let content
</script>

<details>
	<summary>Content</summary>

	<div>
		<label for="content-show"> Show Content? </label><input
			type="checkbox"
			id="content-show"
			bind:checked={content.isShow}
		/>
	</div>

	<div>
		<label for="content">Content Text</label>
		<textarea type="text" id="content" bind:value={content.text} rows="4"></textarea>
	</div>

	<div>
		<label for="font">Font Family</label>
		<select id="font" bind:value={content.font}>
			<option>Poppins</option>
			<option>Montserrat</option>
			<option>Oswald</option>
		</select>
	</div>

	<div>
		<label for="content-uppercase"> Content Uppercase? </label><input
			type="checkbox"
			id="content-uppercase"
			bind:checked={content.isUppercase}
		/>
	</div>

	<div>
		<label for="content-italic"> Content Italic? </label><input
			type="checkbox"
			id="content-italic"
			bind:checked={content.isItalic}
		/>
	</div>

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
		<label for="content-border-radius">
			Content Border Radius: {content.borderRadius}px
		</label>
		<input
			type="range"
			id="content-border-radius"
			bind:value={content.borderRadius}
			min="0"
			max="100"
		/>
	</div>

	<div>
		<label for="content-color">
			Content Color: {content.color}
		</label>
		<input type="color" id="content-color" bind:value={content.color} />
	</div>

	<div>
		<label for="content-background-color">
			Content Background Color: {content.backgroundColor}
		</label>
		<input
			type="color"
			id="content-background-color"
			bind:value={content.backgroundColor}
		/>
	</div>

	<div>
		<label for="content-background-transparent">
			Content Background Transparent?
		</label><input
			type="checkbox"
			id="content-background-transparent"
			bind:checked={content.isBackgroundTransparent}
		/>
	</div>
</details>
