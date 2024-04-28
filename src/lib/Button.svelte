<script>
  export let button
</script>

<details>
	<!-- svelte-ignore a11y-no-redundant-roles -->
	<summary role="button" class="secondary">Button</summary>

	<div>
		<label for="button-show"> Show Button? </label><input
			type="checkbox"
			id="button-show"
			bind:checked={button.isShow}
		/>
	</div>

	<div>
		<label for="button-text">Button Text</label>
		<input type="text" id="button-text" bind:value={button.text} />
	</div>

	<div>
		<label for="font">Font Family</label>
		<select id="font" bind:value={button.font}>
			<option>Poppins</option>
			<option>Montserrat</option>
			<option>Oswald</option>
		</select>
	</div>

	<div>
		<label for="button-href">Button URL</label>
		<input id="button-href" bind:value={button.href} />
	</div>

	<div>
		<label for="button-new-window"> Open in New Window? </label><input
			type="checkbox"
			id="button-new-window"
			bind:checked={button.isOpenBlank}
		/>
	</div>

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
		<label for="button-uppercase"> Button Uppercase? </label>
		<input type="checkbox" id="button-uppercase" bind:checked={button.isUppercase} />
	</div>

	<div>
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

	<div>
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

	<div>
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

	<div>
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

	<div>
		<label for="button-border-width">
			Button Border Width: {button.borderWidth}px
		</label>
		<input
			type="range"
			id="button-border-width"
			bind:value={button.borderWidth}
			min="0"
			max="20"
		/>
	</div>

	<div>
		<label for="button-border-color">
			Button Border Color: {button.borderColor}
		</label>
		<input type="color" id="button-border-color" bind:value={button.borderColor} />
	</div>

	<div>
		<label for="button-background-color">
			Button Background Color: {button.backgroundColor}
		</label>
		<input
			type="color"
			id="button-background-color"
			bind:value={button.backgroundColor}
		/>
	</div>

	<div>
		<label for="button-color">
			Button Color: {button.color}
		</label>
		<input type="color" id="button-color" bind:value={button.color} />
	</div>

	<div>
		<label for="button-border-radius">
			Button Border Radius: {button.borderRadius}px
		</label>
		<input
			type="range"
			id="button-border-radius"
			bind:value={button.borderRadius}
			min="0"
			max="100"
		/>
	</div>

	<div>
		<label for="button-background-transparent">
			Button Background Transparent?
		</label><input
			type="checkbox"
			id="button-background-transparent"
			bind:checked={button.isBackgroundTransparent}
		/>
	</div>
</details>
