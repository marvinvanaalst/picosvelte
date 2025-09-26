<script lang="ts">
	let { children } = $props();
</script>

<div>
	{@render children()}
</div>

<style>
	div {
		display: flex;
		flex-direction: column;
		width: 100%;
		padding-bottom: var(--base-spacing);
	}

	@media screen and (min-width: 42rem) {
		div {
			flex-direction: row;
		}
	}
</style>
