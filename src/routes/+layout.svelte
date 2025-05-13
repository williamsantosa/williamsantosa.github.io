<script lang="ts">
	import '../app.css';
	import NavBar from '$lib/NavBar.svelte';
	import Footer from '$lib/Footer.svelte';
	let { children } = $props();
</script>

<svelte:head>
	<title>William Santosa | Home</title>
	<meta name="description" content="William Santosa - Software Engineer" />
	<link rel="icon" href="/favicon.svg" type="image/svg+xml" />
	<link rel="apple-touch-icon" href="/favicon.svg" type="image/svg+xml" />
	<meta name="theme-color" content="#000000" />
</svelte:head>

<NavBar/>

{@render children()}

<Footer/>
