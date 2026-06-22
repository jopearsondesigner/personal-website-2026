<!--src/lib/components/navbar/Navbar.svelte-->
<script lang="ts">
	import Frame from '../utils/Frame.svelte';
	import { twMerge } from 'tailwind-merge';

	interface $$Props {
		[key: string]: any;
		navClass?: string;
		navDivClass?: string;
		fluid?: boolean;
		class?: string;
		classNavDiv?: string;
		color?: string;
	}

	export let navClass: string = 'px-2 sm:px-4 py-2.5 w-full';
	export let navDivClass: string = 'mx-auto flex flex-wrap justify-between items-center ';
	export let fluid: boolean = false;

	let hidden = true;

	const toggle = () => {
		hidden = !hidden;
	};

	$: frameProps = {
		...$$restProps,
		color: $$restProps.color ?? 'navbar'
	};

	$: navCls = twMerge(navClass, $$props.class);
	$: navDivCls = twMerge(navDivClass, $$props.classNavDiv, (fluid && 'w-full') || 'container');
</script>

<Frame tag="nav" {...frameProps} class={navCls}>
	<div class={navDivCls}>
		<slot {hidden} {toggle} />
	</div>
</Frame>

<!--
@component
[Go to docs](https://flowbite-svelte.com/)
## Props
@prop export let navClass: string = 'px-2 sm:px-4 py-2.5 w-full';
@prop export let navDivClass: string = 'mx-auto flex flex-wrap justify-between items-center ';
@prop export let fluid: boolean = false;
-->
