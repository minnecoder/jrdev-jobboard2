<script lang="ts">
	import Searchbar from '$lib/Searchbar.svelte';
</script>

<div class="container">
	<div class="SideMenu">
		<!-- <SideMenu {jobPosts} /> -->
	</div>
	<div class="main">
		<div class="search">
			<Searchbar />
		</div>
		<div class="jobPosts">
			<!-- <FilteredJobPosts {jobPosts} /> -->
		</div>
	</div>
</div>

<style>
	.container {
		display: flex;
		background: #ececec;
	}
	.SideMenu {
		height: 100%;
		margin: 1rem 0 1rem 1rem;
		border-radius: 10px;
	}

	.jobPosts {
		display: flex;
		flex-wrap: wrap;
	}
</style>
