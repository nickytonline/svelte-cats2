<script context="module" lang="ts">
	export async function load() {
		const response = await fetch('https://cataas.com/api/tags');
		const tags = await response.json();

		return {
			status: response.status,
			props: {
				tags: response.ok && tags.filter((tag: string) => tag !== '')
			}
		};
	}
</script>

<script lang="ts">
	import CatTags from '$lib/CatTags.svelte';

	export let tags: string[] = [];
</script>

<svelte:head>
	<title>Welcome to Svelte Cats 2!</title>
</svelte:head>

<h1>Welcome to Svelte Cats 2!</h1>
<CatTags {tags} />
