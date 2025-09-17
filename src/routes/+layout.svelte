<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.png';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<style>
		@import url('https://fonts.googleapis.com/css2?family=Saira:ital,wght@0,100..900;1,100..900&display=swap');
	</style>
</svelte:head>

{@render children?.()}
