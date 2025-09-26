<script lang="ts">
	import type { Snippet } from 'svelte';
	let {
		children,
		color = 'default'
	}: {
		children: Snippet;
		color?: 'default' | 'contrast' | 'primary' | 'secondary' | 'white' | 'light' | 'dark' | 'black';
	} = $props();
</script>

<h2 class={`${color}`}>
	{@render children()}
</h2>

<style>
	h2 {
		font-size: 1.75rem;
		padding: 0;
		margin: 0 0 var(--base-spacing) 0;
		font-family: var(--font-family);
	}

	.default {
		color: var(--text-default);
	}
	.contrast {
		color: var(--text-contrast);
	}
	.primary {
		color: var(--text-primary);
	}
	.secondary {
		color: var(--text-secondary);
	}
	/* If you want to set a color that stays no matter what the data-theme */
	.white {
		color: var(--l9);
	}
	.light {
		color: var(--light);
	}
	.dark {
		color: var(--dark);
	}
	.black {
		color: var(--l1);
	}
</style>
