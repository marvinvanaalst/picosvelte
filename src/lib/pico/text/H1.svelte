<script lang="ts">
	import type { Snippet } from 'svelte';
	let {
		children,
		lineHeight = 'normal',
		color = 'default'
	}: {
		children: Snippet;
		lineHeight?: 'normal' | 'tight';
		color?: 'default' | 'contrast' | 'primary' | 'secondary' | 'white' | 'light' | 'dark' | 'black';
	} = $props();
</script>

<h1 class={`${color} ${lineHeight}`}>
	{@render children()}
</h1>

<style>
	h1 {
		font-size: 2rem;
		letter-spacing: -2%;
		padding: 0;
		margin: 0 0 var(--base-spacing) 0;
		font-family: var(--font-family);
	}

	@media (min-width: 42rem) {
		h1 {
			font-size: 3rem;
		}
	}
	/* Line height */
	.normal {
		line-height: calc(1.2 * 3rem);
	}
	.tight {
		line-height: 2.5rem;
	}

	/* Colors */
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
