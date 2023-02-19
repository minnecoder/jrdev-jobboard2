<script lang="ts">
	export let label: string;
	export let name: string;
	export let error: string;
	export let placeholder: string = '';
	export let value: string;
	export let type: string = 'text';
	function typeAction(node: any) {
		node.type = type;
	}
</script>

<div class="container">
	<label for={name}>
		{label}

		<input
			use:typeAction
			class={error ? 'error' : 'input'}
			{name}
			id={name}
			{placeholder}
			bind:value
		/>
		<div>
			<span class="inputError">{error}</span>
		</div>
	</label>
</div>

<style>
	.container {
		margin-top: 0.5rem;
		margin-bottom: 1rem;
	}

	.container input {
		width: 100%;
		height: 3rem;
		margin-top: 0.5rem;
		border-radius: 5px;
	}

	.container label > input {
		display: flex;
		flex-direction: column;
	}

	.inputError {
		font-size: 0.8rem;
		color: red;
	}

	.input {
		border: solid 1px rgb(214, 214, 214);
	}

	.error {
		border: solid 1px red;
	}
</style>
