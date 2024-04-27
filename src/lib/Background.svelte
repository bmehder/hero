<script>
	export let app
</script>

<details>
	<summary>Background</summary>

	<div>
		<label for="background-image">Background Image URL</label>
		<input id="background-image" bind:value={app.backgoundImage} />
	</div>

	<div>
		<label for="min-height">Minimum Height</label>
		<input type="range" id="min-height" min="0" max="100" bind:value={app.height} />
	</div>

	<div>
		<label for="spacing">Spacing: {app.gap}rem</label>
		<input type="range" id="spacing" bind:value={app.gap} min="0" max="5" step="0.25" />
	</div>

	<div>
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

	<div>
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
