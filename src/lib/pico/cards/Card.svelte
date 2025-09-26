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

<div class={`card ${color}`}>
	<div class="inner">
		{@render children()}
	</div>
</div>

<style>
	.card {
		margin: var(--base-spacing);
		padding: var(--base-spacing) calc(2 * var(--base-spacing));
		/* border: 1px solid var(--bg-primary); */
		box-shadow:
			0px 18px 36px -18px rgba(0, 0, 0, 0.1),
			0px 30px 45px -30px rgba(50, 50, 93, 0.25);
		width: 26rem;
		max-width: 100%;
		height: 26rem;
		border-radius: 8px;
		transform: scale(1);
		transition: transform 0.3s ease;
		cursor: pointer;
		border-top: 8px var(--primary) solid;
	}
	.card:hover {
		transform: scale(1.03);
		box-shadow:
			0px 18px 36px -18px rgba(0, 0, 0, 0.4),
			0px 30px 45px -30px rgba(50, 50, 93, 0.4);
	}
	.inner {
		height: 100%;
		width: 100%;
		margin: 0 auto;
		padding: calc(2 * var(--base-spacing)) 0;
		display: flex;
		flex-direction: column;
		justify-content: space-around;
	}
	/* Conditionally applied styles */
	.default {
		background-color: var(--bg-lvl2);
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
