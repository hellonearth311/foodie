
<script lang="ts">
  import Accordion from '$lib/Accordion.svelte';
  const faqItems = [
    {
      question: 'Who can participate?',
      answer: 'Anyone who loves coding and food! All skill levels welcome.'
    },
    {
      question: 'What counts as a food-related project?',
      answer: 'Anything that involves food, snacks, recipes, restaurants, or even food-themed games.'
    },
    {
      question: 'How do I log my coding hours?',
      answer: 'Use hackatime!'
    },
    {
      question: 'Can I work in a team?',
      answer: 'Nope! Earn your snacks yourself!'
    }
  ];
</script>

<div class="min-h-screen bg-gray-100 flex items-center justify-center py-12 px-4">
  <div class="w-full max-w-2xl space-y-10">
    <section class="bg-white rounded-xl shadow p-8">
      <h2 class="text-3xl font-bold text-blue-600 mb-4 text-center">Requirements</h2>
      <ul class="mt-6 space-y-3 text-gray-700 list-disc list-inside">
        <li>Build a food-related app or project 🍕</li>
        <li>Code for at least 10 hours 🍔</li>
        <li>Submit before the deadline 🍟</li>
        <li>Have fun 😋</li>
      </ul>
    </section>

    <section class="bg-white rounded-xl shadow p-8">
      <h2 class="text-2xl font-bold text-blue-600 mb-4 text-center">FAQ</h2>
      <Accordion items={faqItems} />
    </section>
  </div>
</div>
