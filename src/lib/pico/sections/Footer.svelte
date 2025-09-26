<script lang="ts">
	import type { Snippet } from 'svelte';
	let {
		children,
		color = 'contrast'
	}: {
		children: Snippet;
		color?: 'default' | 'contrast' | 'primary' | 'secondary' | 'white' | 'light' | 'dark' | 'black';
	} = $props();
</script>

<footer class={`${color}`}>
	<div class="inner">
		{@render children()}
	</div>
</footer>

<style>
	footer {
		margin: 0;
		padding: var(--section-pad) var(--section-pad);
		min-height: 12rem;
		background-color: var(--l1);
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
	@media screen and (min-width: 42rem) {
		footer {
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
		background-color: var(--bg-lvl2);
	}
	.light {
		background-color: var(--bg-lvl1);
	}
	.dark {
		background-color: var(--l2);
	}
	.black {
		background-color: var(--l1);
	}
</style>
