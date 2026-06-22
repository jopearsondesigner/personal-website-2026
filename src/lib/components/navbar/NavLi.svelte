<!--src/lib/components/navbar/NavLi.svelte-->
<script lang="ts">
	import { getContext, onDestroy } from 'svelte';
	import type { Readable, Unsubscriber } from 'svelte/store';
	import { twMerge } from 'tailwind-merge';

	type NavbarContext = {
		activeClass?: string;
		nonActiveClass?: string;
	};

	interface $$Props {
		[key: string]: any;
		href?: string;
		activeClass?: string;
		nonActiveClass?: string;
		class?: string;
	}

	export let href: string = '';
	export let activeClass: string | undefined = undefined;
	export let nonActiveClass: string | undefined = undefined;

	const context = getContext<NavbarContext>('navbarContext') ?? {};
	const activeUrlStore = getContext<Readable<string> | undefined>('activeUrl');

	let navUrl = '';
	let unsubscribe: Unsubscriber | undefined;

	if (activeUrlStore) {
		unsubscribe = activeUrlStore.subscribe((value) => {
			navUrl = value;
		});
	}

	onDestroy(() => {
		if (unsubscribe) unsubscribe();
	});

	$: active = navUrl ? href === navUrl : false;
	$: liClass = twMerge(
		'block py-2 px-4 lg:pl-2 rounded md:border-0',
		active ? activeClass ?? context.activeClass : nonActiveClass ?? context.nonActiveClass,
		$$props.class
	);
</script>

<li>
	{#if href}
		<a
			{href}
			{...$$restProps}
			class={liClass}
			on:blur
			on:change
			on:click
			on:focus
			on:keydown
			on:keypress
			on:keyup
			on:mouseenter
			on:mouseleave
			on:mouseover
		>
			<slot />
		</a>
	{:else}
		<div
			{...$$restProps}
			role="button"
			tabindex="0"
			class={liClass}
			on:blur
			on:change
			on:click
			on:focus
			on:keydown
			on:keypress
			on:keyup
			on:mouseenter
			on:mouseleave
			on:mouseover
		>
			<slot />
		</div>
	{/if}
</li>

<!--
@component
[Go to docs](https://flowbite-svelte.com/)
## Props
@prop export let href: string = '';
@prop export let activeClass: string | undefined = undefined;
@prop export let nonActiveClass: string | undefined = undefined;
-->
