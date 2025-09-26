<script lang="ts">
	import type { Snippet } from 'svelte';
	let {
		href,
		color = 'black',
		children
	}: {
		href: string;
		color?: 'black' | 'white';
		children: Snippet;
	} = $props();
</script>

<a {href} class={`${color}`}>
	{@render children()}
</a>

<style>
	a {
		font-family: sans-serif;
		text-decoration: none;
		text-decoration: currentcolor underline auto;
		transition: var(--transition);
		margin: 0 0 var(--base-spacing) 0;
	}
	a:hover {
		text-decoration: underline;
		color: var(--primary);
	}
	.black {
		color: var(--l1);
	}
	.white {
		color: var(--l9);
	}
</style>
