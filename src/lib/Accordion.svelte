<script lang="ts">
  import { fly } from 'svelte/transition';
  export let items: { question: string; answer: string }[] = [];
  let openIdx: number | null = null;
  function toggle(idx: number) {
    openIdx = openIdx === idx ? null : idx;
  }
</script>

<div class="space-y-4">
  {#each items as item, idx}
    <div>
      <button class="w-full text-left px-4 py-2 rounded bg-gray-100 hover:bg-gray-200 font-semibold text-gray-900 focus:outline-none flex justify-between items-center" on:click={() => toggle(idx)}>
        <span>{item.question}</span>
        <span>{openIdx === idx ? '▲' : '▼'}</span>
      </button>
      {#if openIdx === idx}
        <div transition:fly={{ y: 10, duration: 250 }}>
          <p class="mt-2 text-gray-700 px-4">{item.answer}</p>
        </div>
      {/if}
    </div>
  {/each}
</div>
