<script lang="ts">
	import type { Snippet } from 'svelte';
	let {
		children,
		color = 'primary'
	}: {
		children: Snippet;
		color?: 'default' | 'contrast' | 'primary' | 'secondary' | 'white' | 'light' | 'dark' | 'black';
	} = $props();
</script>

<header class={`${color}`}>
	<div class="inner">
		{@render children()}
	</div>
</header>

<style>
	header {
		margin: 0;
		padding: var(--section-pad) var(--section-pad);
		background-color: var(--primary);
		min-height: 12rem;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
	@media (min-width: 42rem) {
		header {
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
