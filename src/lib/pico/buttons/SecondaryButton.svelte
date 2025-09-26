<script lang="ts">
	import type { Snippet } from 'svelte';
	let {
		children,
		color = 'primary'
	}: {
		children: Snippet;
		color?: 'black' | 'white' | 'primary' | 'secondary' | 'dark';
	} = $props();
</script>

<button class={`${color}`}>
	{@render children()}
</button>

<style>
	button {
		height: 2.5rem;
		width: 9rem;
		font-size: 1rem;
		outline: 0;
		border-radius: 0.5rem;
		transition: var(--transition);
	}
	button:hover {
		transform: scale(1.03);
	}
	button:active {
		transform: scale(1);
		box-shadow: inset 5px 5px 10px -5px rgba(0, 0, 0, 0.5);
	}

	.primary {
		color: var(--primary);
		border: 2px solid var(--primary);
	}
	.secondary {
		color: var(--secondary);
		border: 2px solid var(--secondary);
	}
	.white {
		color: var(--l9);
		border: 1px solid var(--l9);
	}
	.light {
		color: var(--l8);
		border: 1px solid var(--l8);
	}
	.dark {
		color: var(--2);
		border: 2px solid var(--l1);
	}
	.black {
		color: var(--l1);
		border: 2px solid var(--l1);
	}
</style>
