<script lang="ts">
	import Icon from '@iconify/svelte';
	let jobTitle: string = 'Hello';
	let location: string = '';
</script>

<div class="container">
	<h2>Find your first web developer job</h2>
	<h2>Job Title is {jobTitle}</h2>
	<h2>Location is {location}</h2>
	<div class="searchbar">
		<div class="firstSection">
			<div class="icon">
				<Icon icon="material-symbols:search" width="20" height="20" />
			</div>

			<input type="search" bind:value={jobTitle} />
		</div>
		<div class="secondSection">
			<div class="icon">
				<Icon icon="material-symbols:location-on-outline" width="20" height="20" />
			</div>
			<input
				type="search"
				placeholder="Location"
				name="jobLocation"
				id="jobLocation"
				bind:value={location}
			/>
		</div>
	</div>
</div>

<style>
	.container {
		background: linear-gradient(157deg, rgba(117, 156, 255, 1) 0%, rgba(211, 223, 255, 1) 100%);
		border-radius: 10px;
		margin: 1rem 3rem 0 1rem;
		padding: 1.3rem;
	}

	.container h2 {
		text-align: center;
	}

	.searchbar {
		display: flex;
		align-items: center;
		justify-content: center;
		margin-top: 0.5rem;
		padding: 0.5rem 0;
	}

	.icon {
		display: flex;
		justify-content: center;
		align-items: center;
		padding: 0 0.5rem;
	}

	.firstSection {
		display: flex;
		background: white;
		border-right: solid 1px gray;
		border-radius: 10px 0 0 10px;
	}

	.firstSection input[type='search'] {
		padding: 1rem;
		border: 0;
		width: 30rem;
		font: unset;
		font-size: 0.8rem;
	}

	.secondSection {
		display: flex;
		background: white;
		border-radius: 0 10px 10px 0;
	}

	.secondSection input[type='search'] {
		padding: 1rem;
		border: 0;
		border-radius: 10px;
		width: 20rem;
		font: unset;
		font-size: 0.8rem;
	}

	.searchbar input[type='search']:focus {
		outline: none;
	}
</style>
