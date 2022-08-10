<script lang="ts">
	import { page } from '$app/stores';

	const { tag } = $page.params;
</script>

<h1>{tag} Cat</h1>

<main>
	<img
		src={`https://cataas.com/cat/${encodeURIComponent(tag)}`}
		loading="lazy"
		alt={`Random cat image for the tag ${tag}`}
		height="200px"
	/>
</main>
