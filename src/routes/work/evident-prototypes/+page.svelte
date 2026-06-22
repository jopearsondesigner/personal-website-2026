<script lang="ts">
	const projectDetails = [
		{
			label: 'Role',
			value: 'UX/UI prototyping, workflow modeling, product communication'
		},
		{
			label: 'Output',
			value: 'Interactive Figma prototypes, flow models, collaboration concepts'
		},
		{
			label: 'Focus',
			value: 'Reducing uncertainty before engineering implementation'
		}
	];

	const prototypeSections = [
		{
			number: '01',
			title: 'Core Product Prototype',
			description:
				'Interactive product prototype used to explore core workflows, communicate UI direction, and align stakeholders before development.',
			image: '/images/design-prototype.png',
			alt: 'Evident Stack core product prototype',
			link: 'https://www.figma.com/proto/5tW99kYwyM9ujR5c9IN1vN/Evident-Stack?type=design&node-id=2-13304&t=MQFndVuvnmnvWAen-1&scaling=min-zoom&page-id=0%3A1&starting-point-node-id=2%3A13304&mode=design'
		},
		{
			number: '02',
			title: 'Data Prototype',
			description:
				'Prototype focused on making abstract system interactions, data relationships, and technical workflows easier to understand and navigate.',
			image: '/images/data-prototype.png',
			alt: 'Evident Stack data prototype',
			link: 'https://www.figma.com/proto/5tW99kYwyM9ujR5c9IN1vN/Evident-Stack?type=design&node-id=2-17118&t=cKPTu1QG5QGGaVwZ-1&scaling=min-zoom&page-id=2%3A10673&starting-point-node-id=2%3A17118&mode=design'
		},
		{
			number: '03',
			title: 'Collaboration Feature',
			description:
				'Feature prototype focused on team collaboration, shared workflows, and cross-user interaction patterns inside a complex product system.',
			image: '/images/collaboration-prototype.png',
			alt: 'Evident Stack collaboration prototype',
			link: 'https://www.figma.com/proto/5tW99kYwyM9ujR5c9IN1vN/Evident-Stack?type=design&node-id=128-14339&t=z64P4288FnPTGk2o-1&scaling=min-zoom&page-id=2%3A6634&starting-point-node-id=128%3A14339&mode=design'
		}
	];
</script>

<svelte:head>
	<title>Evident Stack Prototypes | Jo Pearson</title>
	<meta
		name="description"
		content="Interactive product prototypes, workflow models, and collaboration concepts for Evident Stack by Jo Pearson."
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
				<p class="jp-kicker text-[#ffebb1]">Prototype Work</p>

				<h1 class="jp-section-title mt-6 max-w-4xl text-5xl text-zinc-100 sm:text-6xl lg:text-7xl">
					Evident Stack Prototypes
				</h1>

				<p class="mt-8 max-w-2xl text-xl leading-relaxed text-zinc-300">
					Interactive product prototypes for exploring complex workflows before engineering.
				</p>
			</div>

			<div class="grid gap-3 sm:grid-cols">
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
					The prototype work helped translate a complex event-driven product system into
					visible workflows, interaction patterns, and product direction. These were not
					just static screens — they were thinking tools for reducing ambiguity before
					front-end implementation.
				</p>
			</div>
		</div>
	</div>
</section>

{#each prototypeSections as section}
	<section class="bg-zinc50 text-zinc-100">
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

					<a
						href={section.link}
						target="_blank"
						rel="noopener noreferrer"
						class="mt-6 inline-flex items-center justify-center rounded border border-[#ffebb1] bg-[#ffebb1] px-5 py-3 text-[11px] font-semibold uppercase tracking-[0.16em] text-zinc-800 transition hover:bg-white"
					>
						View Prototype
					</a>
				</div>
			</div>

			<figure class="overflow-hidden rounded-sm border border-white/10 bg-zinc-900">
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
				Prototype work that turns complex product systems into something teams can see,
				test, and discuss.
			</h2>

			<div class="mt-8 flex flex-wrap gap-3">
				<a
					href="/#work"
					class="inline-flex items-center justify-center rounded border border-[#ffebb1] bg-[#ffebb1] px-5 py-3 text-[11px] font-semibold uppercase tracking-[0.16em] text-zinc-800 transition hover:bg-white"
				>
					Back to Work
				</a>
				<a
					href="/work/evident-brand-system"
					class="inline-flex items-center justify-center rounded border border-zinc-700 px-5 py-3 text-[11px] font-semibold uppercase tracking-[0.16em] text-zinc-400 transition hover:border-zinc-500 hover:text-zinc-200"
				>
					View Brand System
				</a>
			</div>
		</div>
	</div>
</section>
