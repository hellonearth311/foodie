<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<nav class="flex items-center justify-between px-6 py-4 bg-white shadow-md sticky top-0">
	<h1 class="text-xl font-bold text-blue-600">Foodie</h1>
	<ul class="flex space-x-6 text-gray-700 font-medium">
		<li><a href="/" class="hover:text-red-500">Home</a></li>
		<li><a href="/requirements" class="hover:text-red-500">Requirements</a></li>
		<li><a href="https://forms.fillout.com/t/w4S4daqvy4us" class="hover:text-red-500">RSVP</a></li>
	</ul>
</nav>

{@render children?.()}
