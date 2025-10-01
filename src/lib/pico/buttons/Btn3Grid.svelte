<script lang="ts">
	let { children } = $props();
</script>

<div>
	{@render children()}
</div>

<style>
	div {
		width: 100%;
		display: grid;
		gap: var(--base-spacing);
		padding-bottom: var(--base-spacing);
	}

	@media (min-width: 42rem) {
		div {
			grid-template-columns: 1fr 1fr 1fr;
		}
	}
</style>
