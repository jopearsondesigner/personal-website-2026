<script lang="ts">
	import Player from '$lib/components/Player.svelte';
	const projectDetails = [
		{
			label: 'Role',
			value: 'Brand identity, product communication, visual systems, motion direction'
		},
		{
			label: 'Output',
			value: 'Product marks, sub-brand identity, brand guide, motion/explainer assets'
		},
		{
			label: 'Focus',
			value: 'Clarity, modularity, technical communication, SaaS system identity'
		}
	];

	const identityMarks = [
		{
			title: 'Evident Stack',
			description:
				'Product identity for a SaaS platform built around modular architecture, clarity, and scalability.',
			image: '/images/evident-stack-logo.svg',
			alt: 'Evident Stack logo system'
		},
		{
			title: 'Evident Design',
			description:
				'Sub-brand identity for the design layer of Evident Stack, created to distinguish creative tooling within a larger technical ecosystem.',
			image: '/images/evident-design-logo.svg',
			alt: 'Evident Design logo system'
		}
	];

	const motionAssets = [
		{
			title: 'Team Collaboration',
			description:
				'Marketing animation concept showing real-time collaboration and shared workflow visibility.',
			lottie: '/lottie/teamCollaborationHero.json',
			image: '/images/collaboration-animation.svg',
			alt: 'Team collaboration animation preview'
		},
		{
			title: 'Data Layer',
			description:
				'Explainer visual for making abstract data behavior more accessible to non-technical audiences.',
			lottie: '/lottie/DataAnimation.json',
			image: '/images/data-animation.svg',
			alt: 'Data animation preview'
		},
		{
			title: 'Domain Functions',
			description:
				'Visual explanation of domain-level functionality and how business logic operates within the product architecture.',
			lottie: '/lottie/DomainFunctionsAnimation.json',
			image: '/images/domain-functions-animation.svg',
			alt: 'Domain functions animation preview'
		},
		{
			title: 'Deploy',
			description:
				'Motion concept for communicating deployment workflows and technical process clarity.',
			lottie: '/lottie/DeployAnimation.json',
			image: '/images/deploy-animation.svg',
			alt: 'Deploy animation preview'
		},
		{
			title: 'Database',
			description:
				'Visual storytelling around database interactions and backend system relationships.',
			lottie: '/lottie/DatabaseAnimation.json',
			image: '/images/database-animation.svg',
			alt: 'Database animation preview'
		}
	];
</script>

<svelte:head>
	<title>Evident Brand System | Jo Pearson</title>
	<meta
		name="description"
		content="Brand identity, product communication, and motion system work for Evident Stack and Evident Design by Jo Pearson."
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
				<p class="jp-kicker text-[#ffebb1]">Brand System</p>

				<h1 class="jp-section-title mt-6 max-w-4xl text-5xl text-zinc-100 sm:te-6xl lg:text-7xl">
					Evident Brand System
				</h1>

				<p class="mt-8 max-w-2xl text-xl leading-relaxed text-zinc-300">
					Visual identity and product communication system for a technical SaaS ecosystem.
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
					The brand system helped make a complex event-driven SaaS product easier to
					understand, present, and extend. The work connected identity, product layers,
					explainer visuals, and motion assets into a clearer visual language for technical
					and non-technical audiences.
				</p>
			</div>
		</div>
	</div>
</section>

<section class="bg-zinc-950 text-zinc-100">
	<div class="mx-auto max-w-7xl px-6 py-16 sm:px-8 lg:py-20">
		<div class="mb-8 grid gap-6 lg:grid-cols-[0.25fr_0.75fr]">
			<div>
				<p class="jp-kicker text-[#ffebb1]">01</p>
			</div>

			<div>
				<h2 class="jp-section-title text-4xl text-zinc-100 sm:text-5xl">
					Product Identity
				</h2>
				<p class="mt-5 max-w-3xl text-lg leading-relaxed text-zinc-300">
					Two connected marks clarified the relationship between the broader Evident Stack
					platform and the design-focused layer of the product ecosystem.
				</p>
			</div>
		</div>

		<div class="grid gap-6 lg:grid-cols-2">
			{#each identityMarks as mark}
				<article class="overflow-hidden rounded-sm border border-white/10 bg-white">
					<div class="flex min-h-[360px] items-center justify-center p-10">
						<img src={mark.image} alt={mark.alt} class="max-h-40 w-full object-contain" />
					</div>

					<div class="border-t border-zinc-200 bg-zinc-50 p-6 text-zinc-900">
						<p class="jp-kicker text-zinc-500">{mark.title}</p>
						<p class="mt-4 text-base leading-relaxed text-zinc-700">{mark.description}</p>
					</div>
				</article>
			{/each}
		</div>
	</div>
</section>

<section class="bg-zinc-950 text-zinc-100">
	<div class="mx-auto max-w-7xl px-6 py-16 sm:px-8 lg:py-20">
		<div class="mb-8 grid gap-6 lg:grid-cols-[0.25fr_0.75fr]">
			<div>
				<p class="jp-kicker text-[#ffebb1]">02</p>
			</div>

			<div>
				<h2 class="jp-section-title text-4xl text-zinc-100 sm:text-5xl">
					Brand Guide
				</h2>
				<p class="mt-5 max-w-3xl text-lg leading-relaxed text-zinc-300">
					A practical guide defining typography, color, and visual rules so product,
					marketing, and engineering work could stay visually aligned.
				</p>
			</div>
		</div>

		<figure class="overflow-hidden rounded-sm border border-white/10 bg-[#f3f1ec]">
			<img
				src="/images/evident-design-brand-guide.svg"
				alt="Evident brand guide showing typography, color, and visual system rules"
				class="h-auto w-full object-contain"
				loading="lazy"
			/>
		</figure>
	</div>
</section>

<section class="bg-zinc-950 text-zinc-100">
	<div class="mx-auto max-w-7xl px-6 py-16 sm:px-8 lg:py-20">
		<div class="mb-8 grid gap-6 lg:grid-cols-[0.25fr_0.75fr]">
			<div>
				<p class="jp-kicker text-[#ffebb1]">03</p>
			</div>

			<div>
				<h2 class="jp-section-title text-4xl text-zinc-100 sm:text-5xl">
					Motion & Explanation
				</h2>
				<p class="mt-5 max-w-3xl text-lg leading-relaxed text-zinc-300">
					Explainer visuals and motion assets translated technical concepts into clearer,
					more approachable product communication.
				</p>
			</div>
		</div>

		<div class="grid gap-6 md:grid-cols-2">
			{#each motionAssets as asset}
				<article class="overflow-hidden rounded-sm border border-white/10 bg-white/[0.03]">
					<div class="flex min-h-[320px] items-center justify-center bg-zinc-900 p-8">
						{#if asset.lottie}
							<div class="w-full max-w-3xl">
								<Player src={asset.lottie} />
							</div>
						{:else}
							<img
								src={asset.image}
								alt={asset.alt}
								class="max-h-56 w-full object-contain"
								loading="lazy"
							/>
						{/if}
					</div>

					<div class="border-t border-white/10 p-6">
						<p class="jp-kicker text-[#ffebb1]">{asset.title}</p>
						<p class="mt-4 text-base leading-relaxed text-zinc-300">{asset.description}</p>
					</div>
				</article>
			{/each}
		</div>
	</div>
</section>

<section class="border-t border-white/10 bg-zinc-950 text-zinc-100">
	<div class="mx-auto max-w-7xl px-6 py-20 sm:px-8">
		<div class="rounded-2xl border border-white/10 bg-white/[0.03] p-8 sm:p-10">
			<p class="jp-kicker text-[#ffebb1]">Selected Work</p>

			<h2 class="jp-section-title mt-6 max-w-4xl text-4xl text-zinc-100 sm:text-5xl">
				Systems for making complex products easier to see, explain, and build.
			</h2>

			<div class="mt-8 flex flex-wrap gap-3">
				<a
					href="/#work"
					class="inline-flex items-center justify-center rounded border border-[#ffebb1] bg-[#ffebb1] px-5 py-3 text-[11px] font-semibold uppercase tracking-[0.16em] text-zinc-800 transition hover:bg-white"
				>
					Back to Work
				</a>
				<a
					href="/work/beehive-plumbing"
					class="inline-flex items-center justify-center rounded border border-zinc-700 px-5 py-3 text-[11px] font-semibold uppercase tracking-[0.16em] text-zinc-400 transition hover:border-zinc-500 hover:text-zinc-200"
				>
					View Beehive
				</a>
			</div>
		</div>
	</div>
</section>
