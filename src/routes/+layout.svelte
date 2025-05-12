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
	<meta
		name="viewport"
		content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no"
	/>
	<link
		href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<div
	class="navbar text-neutral-content invisible fixed top-0 left-0 z-50 bg-transparent backdrop-blur transition-all duration-300 md:visible"
>
	<div class="navbar-start">
		<p class="text-base-content btn-ghost px-6 text-3xl">William Santosa</p>
	</div>

	<!-- <div class="navbar-center">
		<a class="text-base-content btn btn-ghost text-xl">daisyUI</a>
	</div> -->

	<div class="navbar-end">
		<button class="text-base-content btn btn-ghost text-xl"
			><a
				href="https://www.linkedin.com/in/williamsantosa"
				target="_blank"
				rel="noopener noreferrer">LinkedIn</a
			></button
		>
		<button class="text-base-content btn btn-ghost text-xl"
			><a href="https://github.com/williamsantosa" target="_blank" rel="noopener noreferrer"
				>Github</a
			></button
		>
		<button class="text-base-content btn btn-ghost text-xl">Resume</button>
	</div>
</div>

{@render children()}

<footer class="footer sm:footer-horizontal bg-base-300 text-base-content p-4 items-center flex">
	<div class="flex items-center gap-2">
		<button class="text-base-content btn btn-ghost px-1 text-sm">
			<a
				href="https://github.com/williamsantosa/personal-website"
				target="_blank"
				rel="noopener noreferrer">Source Code</a
			>
		</button>
		<div class="divider divider-horizontal m-0"></div>
		<aside>
			<p class="m-0">© {new Date().getFullYear()} William Santosa - All Rights Reserved</p>
		</aside>
	</div>
	<div class="ml-auto grid-flow-col gap-4">
		<button class="text-base-content btn btn-ghost px-0 text-base">
			<a href="/#">To The Surface</a>
			<img src="/icons/uparrow.svg" alt="Arrow Up" class="inline-block h-4 w-4" />
		</button>
	</div>
</footer>
