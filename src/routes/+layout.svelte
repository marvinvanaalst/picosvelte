<script lang="ts">
	import * as config from '$lib/config';
	import Nav from '$lib/pico/nav/Nav.svelte';
	import NavItem from '$lib/pico/nav/NavItem.svelte';
	import '../app.css';

	let { children } = $props();
</script>

<!-- SEO -->
<svelte:head>
	<meta name="description" content={config.description} />
	<meta property="og:title" content={config.title} />
	<meta property="og:description" content={config.description} />
	<meta property="og:url" content={config.url} />
	<meta property="og:type" content="website" />
	<meta name="twitter:card" content="summary" />
</svelte:head>

<Nav>
	<NavItem href="/" name="Home" />
	<NavItem href="/hexagons" name="Hexagons" />
</Nav>

{@render children()}
