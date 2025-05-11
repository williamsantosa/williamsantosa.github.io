<script lang="ts">
	import ProjectCard from '$lib/ProjectCard.svelte';
	import EmploymentCard from '$lib/EmploymentCard.svelte';

	let textToCopy = 'williamwsantosa@gmail.com';

	function copyText() {
		navigator.clipboard
			.writeText(textToCopy)
			.then(() => {
				alert(`Copied '${textToCopy}' to clipboard!`);
			})
			.catch((err) => {
				console.error('Failed to copy:', err);
			});
	}
</script>

<div class="h-screen w-screen">
	<div class="mx-auto grid h-screen w-screen max-w-[90%] grid-cols-[auto_1fr] items-center gap-20">
		<div class="text-neutral-content flex flex-col items-start justify-center">
			<p class="text-base-content text-7xl leading-none font-bold">William Santosa</p>
			<p class="text-primary-content text-4xl">Software Engineer</p>
			<p class="text-primary-content text-base">
				Hi! I'm a software engineer with professional experience in infrastructure, databases,
				system design, and configurations. I earned my master's degree in computer science from UCLA
				and graduated summa cum laude with a bachelor's degree in computer science from UCSC. In my
				spare time, I enjoy climbing, reading, editing and filming videos with my friends, and
				adopting stuffed animals.
			</p>
			<button
				on:click={copyText}
				class="text-secondary-content btn btn-sm btn-ghost p-0 text-base underline"
			>
				williamwsantosa@gmail.com
				<img src="/icons/clipboard.svg" alt="Copy" class="inline-block h-4 w-4" />
			</button>
			<div class="grid grid-flow-col">
				<button class="text-base-content btn btn-ghost px-0 text-lg">
					<a
						href="mailto:williamwsantosa@gmail.com?subject=Lets connect!"
						target="_blank"
						rel="noopener noreferrer"
					>
						<img src="/icons/email.svg" alt="Email" class="inline-block h-8 w-8" />
					</a>
				</button>
				<button class="text-base-content btn btn-ghost px-1 text-lg">
					<a
						href="https://www.linkedin.com/in/williamsantosa"
						target="_blank"
						rel="noopener noreferrer"
					>
						<img src="/icons/linkedin.svg" alt="LinkedIn" class="inline-block h-8 w-8" />
					</a>
				</button>
				<button class="text-base-content btn btn-ghost px-0 text-lg">
					<a href="https://github.com/williamsantosa" target="_blank" rel="noopener noreferrer">
						<img src="/icons/github.svg" alt="GitHub" class="inline-block h-8 w-8" />
					</a>
				</button>
			</div>
		</div>
		<div class="avatar hidden md:block">
			<div class="mask mask-squircle h-screen w-[90%]">
				<img src="/favicon.svg" alt="William Santosa Logo" />
			</div>
		</div>
	</div>
</div>

<div class="divider m-0"></div>
<div class="flex w-full flex-col px-2 py-1 lg:flex-row">
	<div class="w-full p-2 md:w-1/2">
		<p class="m-2 text-center text-4xl">Now</p>
	</div>
	<div class="w-full p-2 md:w-1/2">
		<p class="m-2 text-center text-4xl hidden md:block">Building</p>
	</div>
</div>

<div class="flex w-full flex-col px-2 py-1 lg:flex-row">
	<EmploymentCard
		position="Software Engineer, Infrastructure Group"
		company="Roblox"
		date="July 2025 - Present"
		description="A web app that allows you to listen to music and podcasts on Spotify."
		imageUrl="/employment/roblox.jpg"
		alt="Album"
		technologies={['React', 'TypeScript', 'Tailwind CSS']}
		buttons={[
			{
				text: 'Listen',
				url: 'https://spotiwhy.com'
			}
		]}
	/>

	<ProjectCard
		title="Not Clash v2"
		description="Second iteration of the original Not Clash discord bot. Facilitates League of Legends matches, stores player and match information in SQLite database, and provides concurrent matchmaking based off Elo rating with many players."
		imageUrl="https://img.daisyui.com/images/stock/photo-1494232410401-ad00d5433cfa.webp"
		alt="League of Legends Character"
		technologies={['JavaScript', 'Node.js', 'SQLite', 'Discord.js']}
		buttons={[
			{
				text: 'GitHub',
				url: 'https://github.com/williamsantosa/Not-Clash-v2'
			}
		]}
	/>
</div>

<div class="divider m-0"></div>
<p class="m-2 text-center text-4xl">Projects</p>

<div class="divider m-0"></div>
<p class="m-2 text-center text-4xl">Experience</p>
