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
				class="flex w-full items-center justify-between rounded-lg border-2 border-accent/20 bg-white/60 px-4 py-3 text-left font-bold text-dark hover:border-accent/40 hover:bg-white/80 focus:outline-none transition"
				on:click={() => toggle(idx)}
			>
				<span>{item.question}</span>
				<span class="size-5 text-accent">
					{#if openIdx === idx}
						<UpArrow />
					{:else}
						<DownArrow />
					{/if}
				</span>
			</button>
			{#if openIdx === idx}
				<div transition:fly={{ y: 10, duration: 250 }}>
					<p class="mt-2 px-4 py-2 text-dark">{item.answer}</p>
				</div>
			{/if}
		</div>
	{/each}
</div>
