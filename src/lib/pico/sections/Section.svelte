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

<section class={`${color}`}>
	<div class="inner">
		{@render children()}
	</div>
</section>

<style>
	section {
		margin: 0;
		padding: var(--section-pad) var(--section-pad);
	}
	@media (min-width: 42rem) {
		section {
			padding: var(--section-pad) 0;
		}
	}
	.inner {
		margin: 0 auto;
		width: 100%;
		max-width: var(--section-width);
	}

	/* Conditionally applied styles */
	.default {
		background-color: var(--bg-lvl1);
	}
	.contrast {
		background-color: var(--bg-contrast);
	}
	.primary {
		background-color: var(--bg-primary);
	}
	.secondary {
		background-color: var(--bg-secondary);
	}
	/* If you want to set a color that stays no matter what the data-theme */
	.white {
		background-color: var(--l9);
	}
	.light {
		background-color: var(--light);
	}
	.dark {
		background-color: var(--dark);
	}
	.black {
		background-color: var(--l1);
	}
</style>
