<script lang="ts">
	const projectDetails = [
		{
			label: 'Role',
			value: 'Strategy, art direction, campaign system, production design'
		},
		{
			label: 'Output',
			value: 'Campaign strategy, visual system, social/display assets'
		},
		{
			label: 'Focus',
			value: 'Trust, care, continuity, and premium home stewardship'
		}
	];

	const projectSections = [
		{
			number: '01',
			title: 'Strategy',
			description:
				'Repositioning Beehive Plumbing from emergency repair to long-term home stewardship — built around care, trust, and continuity.',
			image: '/images/beehive-campaign-strategy.png',
			alt: 'Beehive Plumbing campaign strategy presentation'
		},
		{
			number: '02',
			title: 'System',
			description:
				'A scalable visual system expressing three stages of home life through consistent illustration, structure, and framing.',
			image: '/images/beehive-campaign-expression.png',
			t: 'Beehive Plumbing campaign visual system'
		},
		{
			number: '03',
			title: 'Execution',
			description:
				'Final campaign assets adapted across social, display, and vertical formats while maintaining a calm, premium brand tone.',
			image: '/images/beehive-campaign-assets.png',
			alt: 'Beehive Plumbing campaign execution assets'
		}
	];
</script>

<svelte:head>
	<title>Beehive Plumbing — Campaign Visual System | Jo Pearson</title>
	<meta
		name="description"
		content="Campaign visual system and brand direction for Beehive Plumbing by Jo Pearson."
	/>
</svelte:head>

<section class="bg-zinc-950 text-zinc-100">
	<div class="mx-auto max-w-7xl px-6 py-20 sm:px-8 lg:py-24">
		<a
			href="/#work"
			class="inline-flex items-center text-[11px] font-semibold uppercase tracking-[0.18em] text-zinc-500 transition hover:text-[#ffebb1]"
		>
			← Selected Work
		</a>

		<div class="mt-14 grid gap-12 lg:grid-cols-[0.9fr_1.1fr] lg:items-end">
			<div>
				<p class="jp-kicker text-[#ffebb1]">Campaign Visual System</p>

				<h1 class="jp-section-title mt-6 max-w-4xl text-5xl text-zinc-100 sm:text-6xl lg:text-7xl">
					Beehive Plumbing
				</h1>

				<p class="mt-8 max-w-2xl text-xl leading-relaxed text-zinc-300">
					A service-business campaign system focused on trust, care, continuity, and premium home
					stewardship.
				</p>
			</div>

			<div class="grid gap-3 sm:grid-cols-3">
				{#each projectDetails as item}
					<div class="border-t border-white/10 pt-4">
						<p class="jp-kicker text-zinc-500">{item.label}</p>
						<p class="mt-3 text-sm leading-relaxed text-zinc-300">{item.value}</p>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>

<section class="border-y border-white/10 bg-zinc-950 text-zinc-100">
	<div class="mx-auto max-w-7xl px-6 py-16 sm:px-8 lg:py-20">
		<div class="grid gap-8 lg:grid-cols-[0.45fr_1fr]">
			<div>
				<p class="jp-kicker text-[#ffebb1]">Project Summary</p>
			</div>

			<div class="max-w-3xl">
				<p class="text-2xl leading-relaxed text-zinc-200">
					The campaign reframes plumbing as long-term home care rather than reactive repair. The
					visual system uses quiet illustration, restrained typography, and modular production
					formats to make the brand feel steady, human, and trustworthy.
				</p>
			</div>
		</div>
	</div>
</section>

{#each projectSections as section}
	<section class="bg-zinc-950 text-zinc-100">
		<div class="mx-auto max-w-7xl px-6 py-16 sm:px-8 lg:py-20">
			<div class="mb-8 grid gap-6 lg:grid-cols-[0.25fr_0.75fr]">
				<div>
					<p class="jp-kicker text-[#ffebb1]">{section.number}</p>
				</div>

				<div>
					<h2 class="jp-section-title text-4xl text-zinc-100 sm:text-5xl">
						{section.title}
					</h2>
					<p class="mt-5 max-w-3xl text-lg leading-relaxed text-zinc-300">
						{section.description}
					</p>
				</div>
			</div>

			<figure class="overflow-hidden rounded-sm border border-white/10 bg-[#f3f1ec]">
				<img
					src={section.image}
					alt={section.alt}
					class="h-auto w-full object-contain"
					loading="lazy"
				/>
			</figure>
		</div>
	</section>
{/each}

<section class="border-t border-white/10 bg-zinc-950 text-zinc-100">
	<div class="mx-auto max-w-7xl px-6 py-20 sm:px-8">
		<div class="rounded-2xl border border-white/10 bg-white/[0.03] p-8 sm:p-10">
			<p class="jp-kicker text-[#ffebb1]">Selected Work</p>

			<h2 class="jp-section-title mt-6 max-w-4xl text-4xl text-zinc-100 sm:text-5xl">
				Projects where product thinking, visual systems, and front-end execution need to move
				together.
			</h2>

			<div class="mt-8 flex flex-wrap gap-3">
				<a
					href="/#work"
					class="inline-flex items-center justify-center rounded border border-[#ffebb1] bg-[#ffebb1] px-5 py-3 text-[11px] font-semibold uppercase tracking-[0.16em] text-zinc-800 transition hover:bg-white"
				>
					Back to Work
				</a>
				<a
					href="/#about-me"
					class="inline-flex items-center justify-center rounded border border-zinc-700 px-5 py-3 text-[11px] font-semibold uppercase tracking-[0.16em] text-zinc-400 transition hover:border-zinc-500 hover:text-zinc-200"
				>
					About Jo
				</a>
			</div>
		</div>
	</div>
</section>
