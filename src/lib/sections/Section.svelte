<script lang="ts">
	import type { Snippet } from 'svelte';

	let {
		children,
		color = 'white'
	}: {
		children: Snippet;
		color?: 'black' | 'white' | 'primary' | 'secondary';
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
		padding: var(--section-ypad) 0;
		/* min-height: 20rem; */
	}
	.inner {
		margin: 0 auto;
		max-width: 80ch;
	}
	.black {
		background-color: var(--black);
	}
	.white {
		background-color: var(--white);
	}
	.primary {
		background-color: var(--primary);
	}
	.secondary {
		background-color: var(--secondary);
	}
</style>
