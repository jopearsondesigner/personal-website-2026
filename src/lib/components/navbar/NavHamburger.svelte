<!--src/lib/components/navbar/NavHamburger.svelte-->
<script lang="ts">
	import ToolbarButton from '../toolbar/ToolbarButton.svelte';
	import { twMerge } from 'tailwind-merge';
	import Menu from './Menu.svelte';

	interface $$Props {
		[key: string]: any;
		btnClass?: string;
		menuClass?: string;
		class?: string;
		classMenu?: string;
	}

	export let btnClass: string = 'ml-3 md:hidden';
	export let menuClass: string = 'h-6 w-6 shrink-0';

	$: buttonCls = twMerge(btnClass, $$props.class);
	$: menuCls = twMerge(menuClass, $$props.classMenu);
</script>

<ToolbarButton name="Open main menu" on:click {...$$restProps} class={buttonCls}>
	<Menu class={menuCls} />
</ToolbarButton>

<!--
@component
[Go to docs](https://flowbite-svelte.com/)
## Props
@prop export let btnClass: string = 'ml-3 md:hidden';
@prop export let menuClass: string = 'h-6 w-6 shrink-0';
-->
