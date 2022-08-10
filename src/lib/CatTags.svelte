<script lang="ts">
	export let tags: string[] = [];
</script>

<ul>
	{#each tags as tag}
		<li><a href={`/tags/${encodeURIComponent(tag)}`}>{tag}</a></li>
	{/each}
</ul>

<style>
	ul {
		font-family: 'Roboto', sans-serif;
		display: grid;
		gap: 1rem;
		grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
		list-style: none;
	}

	a::before {
		content: '🐈';
		visibility: hidden;
		margin-right: 0.5rem;
	}

	a {
		position: relative;
		color: rgb(70, 4, 132);
		text-decoration: none;
	}

	a:hover {
		text-decoration: underline;
	}

	a:hover::before {
		visibility: visible;
		content: '🐈';
		margin-right: 0.5rem;
	}
</style>
