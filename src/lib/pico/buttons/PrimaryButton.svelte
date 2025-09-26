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
	button:focus {
		outline: 1px;
	}
	button:active {
		transform: scale(1);
		box-shadow: inset 5px 5px 10px -5px rgba(0, 0, 0, 0.5);
	}

	.primary {
		color: var(--l9);
		border: 1px solid var(--primary);
		background-color: var(--primary);
	}
	.primary:hover {
		box-shadow: inset 0em 0em 0em 10em rgba(0, 0, 0, 0.125);
	}
	.secondary {
		color: var(--l9);
		border: 1px solid var(--secondary);
		background-color: var(--secondary);
	}
	.secondary:hover {
		box-shadow: inset 0em 0em 0em 10em rgba(0, 0, 0, 0.125);
	}
	.dark {
		color: var(--l8);
		border: 1px solid var(--l1);
		background-color: var(--l1);
	}
	.dark:hover {
		box-shadow: inset 0em 0em 0em 10em rgba(255, 255, 255, 0.125);
	}
	.black {
		color: var(--l9);
		border: 1px solid var(--l1);
		background-color: var(--l1);
	}
	.black:hover {
		box-shadow: inset 0em 0em 0em 10em rgba(255, 255, 255, 0.125);
	}
	.white {
		color: var(--primary);
		border: 1px solid var(--l9);
		background-color: var(--l9);
	}
	.white:hover {
		box-shadow: inset 0em 0em 0em 10em rgba(0, 0, 0, 0.125);
	}
</style>
