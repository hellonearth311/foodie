<script lang="ts">
	import Accordion from '$lib/Accordion.svelte';
	const faqItems = [
		{
			question: 'Double dippable with any YSWS?',
			answer: 'Nope!'
		},
		{
			question: 'Who can participate?',
			answer: 'Anyone under 19 in Hack Club!'
		},
		{
			question: 'What counts as a food-related project?',
			answer:
				'Anything that involves food, snacks, recipes, restaurants, or even food-themed games.'
		},
		{
			question: 'Can I work in a team?',
			answer: 'Nope! Earn your food yourself!'
		},
		{
			question: 'Is there a time requirement?',
			answer: 'At least 3 hours please.'
		},
		{
			question: 'When is the deadline?',
			answer: "We haven’t set one yet, but probably sometime around early-mid December 2025, as our sponsor will be able to sponsor in October."
		}	
	];

	const dos = [
		"use ANY framework to build a website that's main concept is related to food (ask in <a href='https://hackclub.slack.com/archives/C09DLGM81E1' class='font-bold'>#foodie-ysws</a> to be sure!)",
		'code for AT LEAST <b>3 hours</b>'
	];
	const donts = ['use AI - not for even the README.md'];
</script>

<div
	class="flex items-center justify-center bg-blue-800 px-4 py-12 font-[Saira] text-white xl:h-screen"
>
	<div class="w-full max-w-2xl space-y-10 xl:max-w-6xl">
		<div class="">
			<h1 class="text-8xl font-bold">foodie</h1>
			<p class="mt-4 text-[2.21rem]">
				build a food-related website/app, get $5 for every hour you spent on it!
			</p>
			<a
				href="https://forms.fillout.com/t/w4S4daqvy4us"
				class="mt-6 inline-block rounded-lg bg-gray-200 px-6 py-3 text-blue-800 transition hover:bg-gray-300"
				target="_blank"
			>
				RSVP now!
			</a>
		</div>
		<div class="grid gap-4 xl:grid-flow-col xl:grid-cols-3 xl:grid-rows-2">
			<section class="rounded-2xl bg-white/90 p-5 text-start xl:col-span-2 xl:max-w-xl">
				<h2 class="mb-4 text-3xl font-bold text-blue-900">Do's and Don'ts</h2>
				<ul class="list-inside list-decimal space-y-2 leading-relaxed">
					{#each dos as d}
						<li class="text-green-600"><span class="font-bold">Do</span> {@html d}</li>
					{/each}
					{#each donts as d}
						<li class="text-red-800"><span class="font-bold">Don't</span> {@html d}</li>
					{/each}
				</ul>
			</section>
			<section class="rounded-2xl bg-white/90 p-5 text-start xl:col-span-2 xl:max-w-xl">
				<h2 class="mb-4 text-3xl font-bold text-blue-900">How It Works</h2>
				<ul class="list-inside list-decimal space-y-2 leading-relaxed text-blue-900">
					<li>
						Setup <a
							href="https://hackatime.hackclub.com"
							class="rounded-xl bg-blue-900 px-2 py-1 font-bold text-white">Hackatime</a
						> and log your coding hours.
					</li>
					<li>For every hour you code, you earn $5 towards delicious meals.</li>
					<li>Redeem your earnings for free food!!</li>
				</ul>
			</section>
			<section
				class="h-[30rem] rounded-2xl bg-white/90 p-5 text-start xl:col-span-20 xl:row-span-2"
			>
				<h2 class="mb-4 text-3xl font-bold text-blue-900">FAQ</h2>
				<Accordion items={faqItems} />
			</section>
		</div>
	</div>
</div>
