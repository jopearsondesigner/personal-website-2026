<!--src/lib/components/navbar/NavBrand.svelte-->
<script lang="ts">
	import { twMerge } from 'tailwind-merge';

	interface $$Props {
		[key: string]: any;
		href?: string;
		class?: string;
	}

	export let href: string = '';

	$: brandCls = twMerge('flex items-center', $$props.class);
</script>

<a {href} {...$$restProps} class={brandCls}>
	<slot />
</a>

<!--
@component
[Go to docs](https://flowbite-svelte.com/)
## Props
@prop export let href: string = '';
-->
