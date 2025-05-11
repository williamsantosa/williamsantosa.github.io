<script lang="ts">
	import '../app.css';

	let { children } = $props();
</script>

<svelte:head>
	<title>William Santosa | Home</title>
	<meta name="description" content="William Santosa - Software Engineer" />
	<link rel="icon" href="/favicon.svg" type="image/svg+xml" />
	<link rel="apple-touch-icon" href="/favicon.svg" type="image/svg+xml" />
	<link rel="manifest" href="/manifest.webmanifest" />
	<meta name="theme-color" content="#000000" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
	<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
</svelte:head>

<div class="navbar text-neutral-content bg-transparent fixed z-50">
	<div class="navbar-start">
		<button class="text-base-content btn btn-ghost text-xl">William Santosa</button>
	</div>

	<!-- <div class="navbar-center">
		<a class="text-base-content btn btn-ghost text-xl">daisyUI</a>
	</div> -->

	<div class="navbar-end">
		<button class="text-base-content btn btn-ghost text-xl"><a href="https://www.linkedin.com/in/williamsantosa" target="_blank" rel="noopener noreferrer">LinkedIn</a></button>
		<button class="text-base-content btn btn-ghost text-xl"><a href="https://github.com/williamsantosa" target="_blank" rel="noopener noreferrer">Github</a></button>
		<button class="text-base-content btn btn-ghost text-xl">Resume</button>
	</div>
</div>

{@render children()}

<footer class="footer sm:footer-horizontal footer-center bg-base-300 text-base-content p-4">
  <aside>
    <p>© {new Date().getFullYear()} William Santosa - All Rights Reserved</p>
  </aside>
</footer>
