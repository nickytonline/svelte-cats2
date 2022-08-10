<script>
	import { page } from '$app/stores';
	console.log($page.params);
	const { index: pageNumber } = $page.params;
</script>

<h1>You are in test integer page {pageNumber}</h1>
YOLO
