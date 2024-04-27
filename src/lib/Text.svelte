<script>
  export let app
</script>

<details>
	<summary>Text</summary>

	<div>
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

	<div>
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
