<script lang="ts">
	import TextInput from '$lib/TextInput.svelte';
	let email = '';
	let password = '';
	let passwordError = '';
	let emailError = '';
	// TODO: Add submit function for form
</script>

<div class="container">
	<div class="left">
		<form class="form">
			<div class="formTitle">
				<h1>Welcome</h1>
			</div>

			<TextInput
				label="Email"
				name="email"
				type="text"
				bind:value={email}
				error={emailError}
			/>
			<TextInput
				label="Password"
				name="password"
				type="password"
				bind:value={password}
				error={passwordError}
			/>
			<input type="submit" value="Sign In" />
		</form>
		<p class="noAccount">
			Don&apos;t have an account?
			<a href="/register">
				<span class="linkText">Create an account</span>
			</a>
		</p>
	</div>
	<div class="right">
		<h1>Right Side</h1>
	</div>
</div>

<style>
	.container {
		display: flex;
	}

	.left {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		height: 100vh;
		width: 50%;
	}

	.right {
		width: 50%;
		background-color: aqua;
	}

	.form {
		display: flex;
		flex-direction: column;
		background: white;
		width: 80%;
		margin-left: 3rem;
		padding: 2rem;
		border-radius: 10px;
	}

	.formTitle {
		margin-bottom: 0.75rem;
	}

	.formTitle h1 {
		margin-bottom: 0;
		font-size: 3rem;
	}

	.noAccount a {
		text-decoration: none;
	}
	.noAccount span {
		color: blue;
		cursor: pointer;
	}

	.form input[type='submit'] {
		margin-top: 1rem;
		padding: 0.5rem;
		height: 3rem;
		border-radius: 5px;
		border: none;
		font: unset;
		font-size: 0.9rem;
		cursor: pointer;
	}

	.noAccount {
		color: rgb(75, 75, 75);
	}

	.noAccount span {
		padding-left: 0.25rem;
	}
</style>
