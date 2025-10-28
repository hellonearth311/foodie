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
			answer: 'Anything that involves food, snacks, recipes, restaurants, or even food-themed games.'
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
			answer: "We haven’t set one yet, but probably sometime around early-mid December 2025."
		}
	];

	const dos = [
		"use ANY language to build an app thats main concept is related to food (ask in <a href='https://hackclub.slack.com/archives/C09DLGM81E1' class='font-bold underline text-accent hover:text-accent-2'>the slack</a> to be sure!)",
		'code for AT LEAST <b>3 hours</b>'
	];
	const donts = ['use AI - not for even the README.md'];
</script>

<div class="flex flex-col min-h-screen">
	<div class="checkered-bar checkered-bar--top"></div>

	<div class="mx-auto w-full max-w-7xl px-4 py-6 md:py-8 flex-1 content-wrap">
		<section class="mb-10 text-center">
		<h1 class="mb-5 text-[4rem] font-bold uppercase leading-tight text-accent md:text-[5rem] font-lcmogi logo">
			FOODIE
		</h1>
		<p class="mx-auto max-w-3xl text-[1.35rem] leading-relaxed text-dark md:text-[1.7rem]">
			build a food-related website/app, get food credits!
		</p>
		<div class="mt-7">
			<a
				href="https://forms.fillout.com/t/w4S4daqvy4us"
				class="inline-block rounded-lg bg-accent px-7 py-3 text-lg font-bold uppercase text-white transition hover:bg-accent-2"
				target="_blank"
			>
				Submit!
			</a>
		</div>
	</section>

	<div class="grid gap-7 lg:grid-cols-2 xl:grid-cols-3">
		<section id="about" class="rounded-2xl border-2 border-accent/30 bg-white/80 p-7 backdrop-blur-sm">
			<h2 class="mb-5 text-[1.7rem] font-bold uppercase text-accent">Do's and Don'ts</h2>
			<ul class="space-y-3 text-base leading-relaxed text-dark">
				{#each dos as d}
					<li class="flex items-start gap-2">
						<span class="mt-1 font-bold text-accent">✓</span>
						<span><span class="font-bold text-accent">Do:</span> {@html d}</span>
					</li>
				{/each}
				{#each donts as d}
					<li class="flex items-start gap-2">
						<span class="mt-1 font-bold text-danger">✗</span>
						<span><span class="font-bold text-danger">Don't:</span> {@html d}</span>
					</li>
				{/each}
			</ul>
		</section>

		<section id="howto" class="rounded-2xl border-2 border-accent/30 bg-white/80 p-7 backdrop-blur-sm">
			<h2 class="mb-5 text-[1.7rem] font-bold uppercase text-accent">How It Works</h2>
			<ol class="space-y-3 text-base leading-relaxed text-dark">
				<li class="flex items-start gap-2">
					<span class="font-bold text-accent">1.</span>
					<span>
						Setup <a
							href="https://hackatime.hackclub.com"
							class="inline-block rounded bg-accent px-2 py-1 font-bold text-white hover:bg-accent-2">Hackatime</a
						> and log your coding hours.
					</span>
				</li>
				<li class="flex items-start gap-2">
					<span class="font-bold text-accent">2.</span>
					<span>Earn food grants based on your Hackatime!</span>
				</li>
				<li class="flex items-start gap-2">
					<span class="font-bold text-accent">3.</span>
					<span>Redeem your earnings for free food!</span>
				</li>
			</ol>
		</section>

		<section id="faq" class="rounded-2xl border-2 border-accent/30 bg-white/80 p-7 backdrop-blur-sm lg:col-span-2 xl:col-span-1 flex flex-col h-[30rem]">
			<h2 class="mb-4 text-[1.7rem] font-bold uppercase text-accent">FAQ</h2>
			<div class="mt-2 overflow-y-auto no-scrollbar flex-1">
				<Accordion items={faqItems} />
			</div>
		</section>
	</div>
	</div>
	<div class="checkered-bar checkered-bar--bottom"></div>
</div>
