<script lang="ts">
	import { fly } from 'svelte/transition';
	import UpArrow from './assets/UpArrow.svelte';
	import DownArrow from './assets/DownArrow.svelte';
	export let items: { question: string; answer: string }[] = [];
	let openIdx: number | null = null;
	function toggle(idx: number) {
		openIdx = openIdx === idx ? null : idx;
	}
</script>

<div class="space-y-4">
	{#each items as item, idx}
		<div>
			<button
				class="flex w-full items-center justify-between rounded bg-gray-100 px-4 py-2 text-left font-semibold text-gray-900 hover:bg-gray-200 focus:outline-none"
				on:click={() => toggle(idx)}
			>
				<span>{item.question}</span>
				<span class="size-4">
					{#if openIdx === idx}
						<UpArrow />
					{:else}
						<DownArrow />
					{/if}
				</span>
			</button>
			{#if openIdx === idx}
				<div transition:fly={{ y: 10, duration: 250 }}>
					<p class="mt-2 px-4 text-gray-700">{item.answer}</p>
				</div>
			{/if}
		</div>
	{/each}
</div>
