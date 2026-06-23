<script lang="ts">
	const heroFeaturedProjects = [
		{
			title: 'FollowFlow',
			label: 'Featured Work',
			description: 'AI follow-up command center for founder-led service businesses.',
			meta: 'Product strategy · SaaS UI · SvelteKit · Front-end build',
			image: '/images/followflow-landing-page.png',
			alt: 'FollowFlow landing page and dashboard preview',
			primaryLink: {
				label: 'View Dashboard',
				href: 'https://followflow-demo.netlify.app/dashboard',
				external: true
			},
			links: [
				{
					label: 'View Dashboard',
					href: 'https://followflow-demo.netlify.app/dashboard',
					external: true,
					primary: true
				},
				{
					label: 'Landing Page',
					href: 'https://followflow-website.netlify.app/',
					external: true
				},
				{
					label: 'Source',
					href: 'https://github.com/jopearsondesigner/followflow',
					external: true
				}
			]
		},
		{
			title: 'The Validation Movement',
			label: 'Featured Work',
			description:
				'Emotionally intelligent website concept for validation, nervous-system support, and softer digital spaces.',
			meta: 'Editorial web design · Emotional UX · SvelteKit · Front-end build',
			image: '/images/the-validation-movement-website.png',
			alt: 'The Validation Movement website preview',
			primaryLink: {
				label: 'View Site',
				href: 'https://the-validation-movement.netlify.app/',
				external: true
			},
			links: [
				{
					label: 'View Site',
					href: 'https://the-validation-movement.netlify.app/',
					external: true,
					primary: true
				},
				{
					label: 'InnerAnchor',
					href: 'https://the-validation-movement.netlify.app/inner-anchor',
					external: true
				},
				{
					label: 'Source',
					href: 'https://github.com/jopearsondesigner/the-validation-movement',
					external: true
				}
			]
		}
	];

	let activeFeaturedIndex = 0;

	$: activeFeaturedProject = heroFeaturedProjects[activeFeaturedIndex];

	$: nextFeaturedProject =
		heroFeaturedProjects[(activeFeaturedIndex + 1) % heroFeaturedProjects.length];

	const showNextFeatured = () => {
		activeFeaturedIndex = (aveFeaturedIndex + 1) % heroFeaturedProjects.length;
	};

	const showPreviousFeatured = () => {
		activeFeaturedIndex =
			(activeFeaturedIndex - 1 + heroFeaturedProjects.length) % heroFeaturedProjects.length;
	};

	type ProjectLink = {
		label: string;
		href: string;
		external?: boolean;
		primary?: boolean;
	};

	type Project = {
		title: string;
		type: string;
		description: string;
		image: string;
		alt: string;
		tags: string[];
		links: ProjectLink[];
		featured?: boolean;
	};

	const featuredProjects: Project[] = [
		{
			title: 'FollowFlow',
			type: 'AI Follow-Up Command Center',
			description:
				'A self-initiated SaaS concept for founder-led service businesses. Designed and built end to end to show who to follow up with next, why it matters, what revenue is at risk, and what message to send.',
			image: '/images/followflow-dashboard.png',
			alt: 'FollowFlow dashboard interface showing lead prioritization and follow-up signals',
			tags: ['SaaS UI', 'AI Product Thinking', 'SvelteKit', 'Tailwind', 'Dashboard Design'],
			featured: true,
			links: [
				{
					label: 'View Dashboard',
					href: 'https://followflow-demo.netlify.app/dashboard',
					external: true,
					primary: true
				},
				{
					label: 'Landing Page',
					href: 'https://followflow-website.netlify.app/',
					external: true
				},
				{
					label: 'Source',
					href: 'https://github.com/jopearsondesigner/followflow',
					external: true
				}
			]
		},
		{
			title: 'Wanderlust Travel Adventures',
			type: 'Travel Advisor Website',
			description:
				'A polished travel advisor website rebuilt around premium positioning, personalized planning, clear inquiry paths, responsive design, and a live custom-domain deployment.',
			image: '/images/wanderlust-travel-adventures.png',
			alt: 'Wanderlust Travel Adventures website hero section',
			tags: ['Live Website', 'Premium Web Design', 'SvelteKit', 'Netlify', 'Client Delivery'],
			links: [
				{
					label: 'View Live Site',
					href: 'https://wanderlusttraveladventures.com/',
					external: true,
					primary: true
				}
			]
		},
		{
			title: 'Evident Stack',
			type: 'SaaS UI & Front-End System',
			description:
				'Product and front-end work for a complex event-driven SaaS system. Used visual systems, prototypes, and interface design to make technical workflows clearer and easier to communicate.',
			image: '/images/slide-evident-stack.png',
			alt: 'Evident Stack product and front-end work',
			tags: ['SaaS', 'Design Systems', 'Complex UI', 'Prototyping', 'Front-End'],
			links: [
				{
					label: 'Brand System',
					href: '/work/evident-brand-system',
					primary: true
				},
				{
					label: 'SaaS Demo',
					href: 'https://evident-stack-demo.netlify.app/',
					external: true
				},
				{
					label: 'Website',
					href: 'https://evident-stack.netlify.app/',
					external: true
				},
				{
					label: 'Prototype Work',
					href: '/work/evident-prototypes'
				}
			]
		},
		{
			title: 'Beehive Plumbing',
			type: 'Campaign Visual System',
			description:
				'A service-business campaign system focused on trust, care, continuity, and premium home stewardship. Built as a scalable visual direction across strategy, system, and production assets.',
			image: '/images/beehive-campaign-assets.png',
			alt: 'Beehive Plumbing campaign assets and visual system',
			tags: ['Brand Strategy', 'Campaign Design', 'Art Direction', 'Production Design'],
			links: [
				{
					label: 'View Project',
					href: '/work/beehive-plumbing',
					primary: true
				}
			]
		},
		{
			title: 'InnerAnchor / The Validation Movement',
			type: 'Emotional UX Concepts',
			description:
				'Mission-driven emotional regulation and mental-health-adjacent product concepts using careful language, atmosphere, interaction pacing, and emotionally intelligent UX.',
			image: '/images/the-validation-movement-inner-anchor.png',
			alt: 'InnerAnchor emotional regulation interface concept',
			tags: ['Emotional UX', 'Visual Storytelling', 'SvelteKit', 'Editorial Design'],
			links: [
				{
					label: 'View InnerAnchor',
					href: 'https://the-validation-movement.netlify.app/inner-anchor',
					external: true,
					primary: true
				},
				{
					label: 'Landing Page',
					href: 'https://the-validation-movement.netlify.app/',
					external: true
				}
			]
		}
	];

	const capabilities = [
		{
			title: 'Product & SaaS UI',
			description: 'Dashboards, prototypes, workflows, decision systems, and interface clarity.'
		},
		{
			title: 'Brand & Visual Systems',
			description: 'Identity, typography, campaign direction, scalable design language, and polish.'
		},
		{
			title: 'Web Design & Front-End',
			description: 'Responsive websites, SvelteKit, React, Tailwind, CSS, and deployed builds.'
		},
		{
			title: 'AI-Enabled Creative Direction',
			description:
				'Using AI as leverage while owning judgment, structure, product strategy, and final quality.'
		}
	];
</script>

<svelte:head>
	<title>Jo Pearson — Designer & Front-End Builder</title>
	<meta
		name="description"
		content="Jo Pearson is a designer and front-end builder who turns complex ideas into clear visual systems, polished interfaces, and shipped websites/products."
	/>
</svelte:head>

<section
	class="relative overflow-hidden bg-zinc-950 border-b border-zinc-800"
	aria-labelledby="home-hero-title"
>
	<div class="absolute inset-0 opacity-70" aria-hidden="true">
		<div
			class="absolute left-1/2 top-0 h-[520px] w-[520px] -translate-x-1/2 rounded-full bg-[#ff05bd]/10 blur-3xl"
		/>
		<div
			class="absolute right-0 top-32 h-[420px] w-[420px] rounded-full bg-[#ffebb1]/10 blur-3xl"
		/>
		<div
			class="absolute left-0 bottom-0 h-[360px] w-[360px] rounded-full bg-cyan-400/10 blur-3xl"
		/>
	</div>

	<div class="relative sm:container mx-auto px-6 py-20 lg:py-28">
		<div class="grid gap-12 lg:grid-cols-12 lg:items-center">
			<div class="lg:col-span-7 lg:-translate-y-6 xl:-translate-y-8">
				<p class="jp-kicker mb-5 text-[#ffebb1]">Designer & Front-End Builder</p>

				<h1
					id="home-hero-title"
					class="jp-poster-display text-5xl sm:text-6xl lg:text-[5.5rem] text-zinc-100"
				>
					Jo Pearson
				</h1>

				<p class="mt-10 max-w-3xl text-xl sm:text-2xl lg:text-3xl leading-snug text-zinc-200">
					Visual systems, interfaces, and front-end builds for complex ideas that need to become
					clear, usable, and real.
				</p>

				<p class="mt-7 max-w-2xl text-base sm:text-lg leading-relaxed text-zinc-400">
					Brand, SaaS UI, web design, and front-end implementation — shaped with taste, judgment,
					and code.
				</p>

				<div class="mt-10 flex flex-wrap gap-3">
					<a
						href="#work"
						class="inline-flex items-center justify-center rounded border border-[#ffebb1] bg-gradient-to-t from-[#ffebb1] via-[#ffebb1] to-white px-5 py-3 text-xs font-semibold uppercase tracking-[0.18em] text-zinc-700 shadow-lg shadow-black/30 transition hover:scale-[1.02]"
					>
						View Work
					</a>
					<a
						href="mailto:jopearsondesigner@gmail.com"
						class="inline-flex items-center justify-center rounded border border-zinc-700 bg-white/[0.04] px-5 py-3 text-xs font-semibold uppercase tracking-[0.18em] text-zinc-300 transition hover:border-zinc-500 hover:bg-white/[0.07]"
					>
						Contact Me
					</a>
					<a
						href="https://github.com/jopearsondesigner"
						target="_blank"
						rel="noopener noreferrer"
						class="inline-flex items-center justify-center rounded border border-zinc-800 px-5 py-3 text-xs font-semibold uppercase tracking-[0.18em] text-zinc-500 transition hover:border-zinc-600 hover:text-zinc-300"
					>
						GitHub
					</a>
				</div>
			</div>

			<div class="lg:col-span-5">
				<figure class="relative">
					<a
						href={activeFeaturedProject.primaryLink.href}
						target={activeFeaturedProject.primaryLink.external ? '_blank' : undefined}
						rel={activeFeaturedProject.primaryLink.external ? 'noopener noreferrer' : undefined}
						class="group block overflow-hidden rounded-xl border border-white/10 bg-zinc-950 shadow-2xl shadow-black/30"
						aria-label={activeFeaturedProject.primaryLink.label}
					>
						<img
							src={activeFeaturedProject.image}
							alt={activeFeaturedProject.alt}
							class="aspect-[16/9] w-full object-cover opacity-85 transition duration-500 group-hover:scale-[1.015] group-hover:opacity-100"
						/>
					</a>

					<figcaption class="mt-5 border-t border-white/10 pt-5">
						<div class="flex items-center justify-between gap-4">
							<p class="jp-kicker text-[#ffebb1]">{activeFeaturedProject.label}</p>
							<p class="text-[11px] font-semibold uppercase tracking-[0.18em] text-zinc-600">
								{activeFeaturedIndex + 1} / {heroFeaturedProjects.length}
							</p>
						</div>

						<div class="mt-4 grid gap-5 md:grid-cols-[0.52fr_1fr] md:items-start">
							<h2 class="jp-project-title text-3xl text-zinc-100 sm:text-4xl">
								{activeFeaturedProject.title}
							</h2>

							<div>
								<p class="text-base leading-relaxed text-zinc-300">
									{activeFeaturedProject.description}
								</p>

								<p class="mt-4 text-sm leading-relaxed text-zinc-500">
									{activeFeaturedProject.meta}
								</p>

								<div class="mt-6 flex flex-wrap gap-3">
									{#each activeFeaturedProject.links as link}
										<a
											href={link.href}
											target={link.external ? '_blank' : undefined}
											rel={link.external ? 'noopener noreferrer' : undefined}
											class={link.primary
												? 'inline-flex items-center justify-center rounded border border-[#ffebb1] bg-[#ffebb1] px-4 py-2.5 text-[11px] font-semibold uppercase tracking-[0.16em] text-zinc-800 transition hover:bg-white'
												: 'inline-flex items-center justify-center rounded border border-zinc-700 px-4 py-2.5 text-[11px] font-semibold uppercase tracking-[0.16em] text-zinc-400 transition hover:border-zinc-500 hover:text-zinc-200'}
										>
											{link.label}
										</a>
									{/each}
								</div>
							</div>
						</div>

						<div class="mt-6 flex justify-end border-t border-white/10 pt-4">
							<button
								type="button"
								on:click|preventDefault|stopPropagation={() => {
									activeFeaturedIndex =
										(activeFeaturedIndex + 1) % heroFeaturedProjects.length;
								}}
								class="inline-flex items-center justify-center rounded border border-zinc-700 px-4 py-2.5 text-[11px] font-semibold uppercase tracking-[0.16em] text-[#ffebb1] transition hover:border-[#ffebb1] hover:text-white"
								aria-label="Show next featured project"
							>
								Next: {nextFeaturedProject.title} →
							</button>
						</div>
	</div>
</section>

<section id="work" class="bg-zinc-950 py-16 lg:py-24" aria-labelledby="featured-work-title">
	<div class="sm:container mx-auto px-6">
		<div class="mb-12 max-w-3xl">
			<p class="jp-kicker mb-4 text-[#ffebb1]">Featured Work</p>
			<h2
				id="featured-work-title"
				class="jp-section-title text-3xl sm:text-4xl lg:text-5xl text-zinc-100"
			>
				Selected work across product, web, and visual systems.
			</h2>
			<p class="mt-5 text-base sm:text-lg leading-relaxed text-zinc-400">
				Selected projects across SaaS UI, live websites, campaign systems, prototypes, and emotional
				product concepts.
			</p>
		</div>

		<div class="grid gap-6 lg:grid-cols-2">
			{#each featuredProjects as project}
				<article
					class={`group overflow-hidden rounded-3xl border border-white/10 bg-white/[0.035] shadow-xl shadow-black/20 transition hover:border-[#ffebb1]/40 hover:bg-white/[0.055] ${
						project.featured ? 'lg:col-span-2' : ''
					}`}
				>
					<div class={`grid gap-0 ${project.featured ? 'lg:grid-cols-2' : ''}`}>
						<div class="relative min-h-[260px] overflow-hidden bg-zinc-900">
							<img
								src={project.image}
								alt={project.alt}
								class="h-full min-h-[260px] w-full object-cover object-center opacity-90 transition duration-500 group-hover:scale-[1.025] group-hover:opacity-100"
							/>
							<div
								class="absolute inset-0 bg-gradient-to-t from-zinc-950/60 via-transparent to-transparent"
							/>
						</div>

						<div class="flex flex-col justify-between p-6 sm:p-8 lg:p-10">
							<div>
								<p class="text-xs uppercase tracking-[0.28em] text-[#ffebb1]">{project.type}</p>
								<h3 class="jp-project-title mt-4 text-3xl sm:text-4xl text-zinc-100">
									{project.title}
								</h3>
								<p class="mt-5 text-sm sm:text-base leading-relaxed text-zinc-400">
									{project.description}
								</p>

								<div class="mt-6 flex flex-wrap gap-2">
									{#each project.tags as tag}
										<span
											class="rounded bg-zinc-800 px-3 py-1 text-[10px] uppercase tracking-[0.18em] text-zinc-300"
										>
											{tag}
										</span>
									{/each}
								</div>
							</div>

							<div class="mt-8 flex flex-wrap gap-3">
								{#each project.links as link}
									<a
										href={link.href}
										target={link.external ? '_blank' : undefined}
										rel={link.external ? 'noopener noreferrer' : undefined}
										class={`inline-flex items-center justify-center rounded px-4 py-2 text-[11px] font-semibold uppercase tracking-[0.16em] transition ${
											link.primary
												? 'border border-[#ffebb1] bg-[#ffebb1] text-zinc-800 hover:bg-white'
												: 'border border-zinc-700 text-zinc-400 hover:border-zinc-500 hover:text-zinc-200'
										}`}
									>
										{link.label}
									</a>
								{/each}
							</div>
						</div>
					</div>
				</article>
			{/each}
		</div>
	</div>
</section>

<section
	class="border-y border-zinc-800 bg-white/[0.04] py-16 lg:py-20"
	aria-labelledby="capabilities-title"
>
	<div class="sm:container mx-auto px-6">
		<div class="grid gap-10 lg:grid-cols-12">
			<div class="lg:col-span-4">
				<p class="jp-kicker mb-4 text-[#ffebb1]">Capabilities</p>
				<h2 id="capabilities-title" class="jp-section-title text-3xl sm:text-4xl text-zinc-100">
					Where the work gets useful.
				</h2>
			</div>

			<div class="grid gap-4 sm:grid-cols-2 lg:col-span-8">
				{#each capabilities as capability}
					<div class="rounded-2xl border border-white/10 bg-zinc-950/70 p-6">
						<h3 class="text-sm font-semibold uppercase tracking-[0.22em] text-zinc-100">
							{capability.title}
						</h3>
						<p class="mt-4 text-sm leading-relaxed text-zinc-400">{capability.description}</p>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>

<section id="about-me" class="bg-zinc-950 py-16 lg:py-24" aria-labelledby="about-title">
	<div class="sm:container mx-auto px-6">
		<div class="grid gap-10 lg:grid-cols-12 lg:items-center">
			<div class="lg:col-span-4">
				<div class="mx-auto max-w-[300px] rounded-full border-[28px] border-white/[0.025]">
					<div class="overflow-hidden rounded-full border-[28px] border-white/[0.06]">
						<img
							src="/images/jo-5433.png"
							alt="Jo Pearson"
							class="aspect-square w-full object-cover"
						/>
					</div>
				</div>
			</div>

			<div class="lg:col-span-8">
				<p class="jp-kicker mb-4 text-[#ffebb1]">About</p>
				<h2 id="about-title" class="jp-section-title text-3xl sm:text-4xl text-zinc-100">
					Designer-builder with range.
				</h2>

				<div class="mt-6 max-w-3xl space-y-5 text-base sm:text-lg leading-relaxed text-zinc-400">
					<p>
						I’m a Salt Lake City designer and front-end builder with experience across SaaS,
						branding, UX/UI, marketing sites, prototypes, and production-ready front-end work.
					</p>
					<p>
						I’m strongest when I can move between strategy, visual systems, interface design, and
						implementation — especially when the work needs both taste and technical follow-through.
					</p>
					<p>
						I use AI the way a strong designer uses any leverage tool: to accelerate exploration,
						critique, writing, and implementation — while owning the product strategy, visual
						direction, design decisions, front-end execution, and final quality bar.
					</p>
				</div>

				<div class="mt-8 flex flex-wrap gap-2">
					<span
						class="rounded bg-zinc-800 px-3 py-1 text-[11px] uppercase tracking-[0.18em] text-zinc-300"
						>Figma</span
					>
					<span
						class="rounded bg-zinc-800 px-3 py-1 text-[11px] uppercase tracking-[0.18em] text-zinc-300"
						>SvelteKit</span
					>
					<span
						class="rounded bg-zinc-800 px-3 py-1 text-[11px] uppercase tracking-[0.18em] text-zinc-300"
						>React</span
					>
					<span
						class="rounded bg-zinc-800 px-3 py-1 text-[11px] uppercase tracking-[0.18em] text-zinc-300"
						>Tailwind</span
					>
					<span
						class="rounded bg-zinc-800 px-3 py-1 text-[11px] uppercase tracking-[0.18em] text-zinc-300"
						>HTML</span
					>
					<span
						class="rounded bg-zinc-800 px-3 py-1 text-[11px] uppercase tracking-[0.18em] text-zinc-300"
						>CSS</span
					>
					<span
						class="rounded bg-zinc-800 px-3 py-1 text-[11px] uppercase tracking-[0.18em] text-zinc-300"
						>JavaScript</span
					>
					<span
						class="rounded bg-zinc-800 px-3 py-1 text-[11px] uppercase tracking-[0.18em] text-zinc-300"
						>Design Systems</span
					>
					<span
						class="rounded bg-zinc-800 px-3 py-1 text-[11px] uppercase tracking-[0.18em] text-zinc-300"
						>Branding</span
					>
				</div>
			</div>
		</div>
	</div>
</section>

<section
	id="resume"
	class="border-y border-zinc-800 bg-white/[0.04] py-16 lg:py-20"
	aria-labelledby="resume-title"
>
	<div class="sm:container mx-auto px-6">
		<div class="grid gap-8 lg:grid-cols-12 lg:items-center">
			<div class="lg:col-span-7">
				<p class="jp-kicker mb-4 text-[#ffebb1]">Résumé Snapshot</p>
				<h2 id="resume-title" class="jp-section-title text-3xl sm:text-4xl text-zinc-100">
					A career built between design and implementation.
				</h2>
				<p class="mt-5 max-w-3xl text-base sm:text-lg leading-relaxed text-zinc-400">
					My background spans SaaS product UI, interactive prototypes, marketing websites, brand
					systems, HTML/CSS/JavaScript implementation, and production design work.
				</p>
			</div>

			<div class="lg:col-span-5">
				<div class="rounded-2xl border border-white/10 bg-zinc-950/70 p-6">
					<div class="space-y-5">
						<div>
							<p class="text-sm font-semibold uppercase tracking-[0.18em] text-zinc-100">
								Lead Designer — Evident Systems
							</p>
							<p class="mt-2 text-sm text-zinc-500">
								SaaS UI, design systems, prototypes, front-end implementation
							</p>
						</div>
						<div>
							<p class="text-sm font-semibold uppercase tracking-[0.18em] text-zinc-100">
								Freelance Designer & Developer
							</p>
							<p class="mt-2 text-sm text-zinc-500">
								Web, branding, campaigns, landing pages, production assets
							</p>
						</div>
						<div>
							<p class="text-sm font-semibold uppercase tracking-[0.18em] text-zinc-100">
								UX / Web / Graphic Design Background
							</p>
							<p class="mt-2 text-sm text-zinc-500">
								Younique, CR England, CMN Hospitals, AdvancedMD, Red Olive
							</p>
						</div>
					</div>

					<div class="mt-7 flex flex-wrap gap-3">
						<a
							href="mailto:jopearsondesigner@gmail.com"
							class="inline-flex items-center justify-center rounded border border-[#ffebb1] bg-[#ffebb1] px-4 py-2 text-[11px] font-semibold uppercase tracking-[0.16em] text-zinc-800 transition hover:bg-white"
						>
							Request Résumé
						</a>
						<a
							href="https://www.linkedin.com/in/jopearsondesigner/"
							target="_blank"
							rel="noopener noreferrer"
							class="inline-flex items-center justify-center rounded border border-zinc-700 px-4 py-2 text-[11px] font-semibold uppercase tracking-[0.16em] text-zinc-400 transition hover:border-zinc-500 hover:text-zinc-200"
						>
							LinkedIn
						</a>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<section class="bg-zinc-950 py-16 lg:py-24" aria-labelledby="cta-title">
	<div class="sm:container mx-auto px-6">
		<div
			class="overflow-hidden rounded-3xl border border-white/10 bg-gradient-to-br from-white/[0.08] via-zinc-900 to-zinc-950 p-8 sm:p-10 lg:p-14"
		>
			<div class="max-w-3xl">
				<p class="jp-kicker mb-4 text-[#ffebb1]">Let’s Build</p>
				<h2 id="cta-title" class="jp-section-title text-3xl sm:text-4xl lg:text-5xl text-zinc-100">
					Projects where product thinking, visual systems, and front-end execution need to move
					together.
				</h2>
				<p class="mt-5 text-base sm:text-lg leading-relaxed text-zinc-400">
					I’m available for hands-on design, front-end, web, UI, branding, and hybrid
					designer-builder opportunities.
				</p>

				<div class="mt-8 flex flex-wrap gap-3">
					<a
						href="mailto:jopearsondesigner@gmail.com"
						class="inline-flex items-center justify-center rounded border border-[#ffebb1] bg-gradient-to-t from-[#ffebb1] via-[#ffebb1] to-white px-5 py-3 text-xs font-semibold uppercase tracking-[0.18em] text-zinc-700 shadow-lg shadow-black/30 transition hover:scale-[1.02]"
					>
						Contact Me
					</a>
					<a
						href="https://github.com/jopearsondesigner"
						target="_blank"
						rel="noopener noreferrer"
						class="inline-flex items-center justify-center rounded border border-zinc-700 bg-white/[0.04] px-5 py-3 text-xs font-semibold uppercase tracking-[0.18em] text-zinc-300 transition hover:border-zinc-500 hover:bg-white/[0.07]"
					>
						View GitHub
					</a>
					<a
						href="#work"
						class="inline-flex items-center justify-center rounded border border-zinc-800 px-5 py-3 text-xs font-semibold uppercase tracking-[0.18em] text-zinc-500 transition hover:border-zinc-600 hover:text-zinc-300"
					>
						Back to Work
					</a>
				</div>
			</div>
		</div>
	</div>
</section>
