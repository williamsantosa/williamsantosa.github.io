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
		<div class="avatar hidden lg:block">
			<div class="mask mask-squircle h-screen w-[90%]">
				<img src="/favicon.svg" alt="William Santosa Logo" />
			</div>
		</div>
	</div>
</div>

<div class="divider m-0"></div>
<div class="flex w-full flex-col px-2 py-1 lg:flex-row">
	<div class="w-full p-2 lg:w-1/2">
		<p class="m-2 text-center text-4xl">Now</p>
	</div>
	<div class="w-full p-2 lg:w-1/2">
		<p class="m-2 hidden text-center text-4xl lg:block">Building</p>
	</div>
</div>

<div class="flex w-full flex-col px-2 py-1 lg:flex-row">
	<EmploymentCard
		position="Software Engineer, Infrastructure Group"
		company="Roblox"
		date="July 2025 - Present"
		description=""
		imageUrl="/employment/roblox.jpg"
		alt="Album"
		technologies={[]}
		buttons={[
			{
				text: 'About Us',
				url: 'https://corp.roblox.com/'
			}
		]}
	/>
	
	<div class="divider divider-horizontal m-0"></div>

	<ProjectCard
		title="Not Clash v2"
		date="January 2023"
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
<p class="m-2 text-center text-4xl">Employment</p>

<div class="flex w-full flex-col px-2 py-1 lg:flex-row">
	<EmploymentCard
		position="Software Engineer Intern"
		company="Roblox"
		date="July 2024 - September 2024"
		description="Unified two high-throughput products handling 220K+ requests/sec per region. Designed API endpoints and MSSQL components to migrate 1M+ rows of data to a new system. Built an exporter to convert legacy data into configuration-as-code. Automated data publishing with Python and GitHub Actions. Developed cross-environment endpoints in collaboration with infra teams."
		imageUrl="/employment/roblox.jpg"
		alt="Album"
		technologies={['C#', 'Python', '.NET Core', 'GitHub Action', 'MSSQL']}
		buttons={[
			{
				text: 'Website',
				url: 'https://corp.roblox.com/'
			}
		]}
	/>

	<EmploymentCard
		position="Software Engineering Intern"
		company="Maxar Technologies"
		date="June 2022 - September 2022"
		description="Designed and developed internal system feature for satellites including the Galaxy-31 and Galaxy-32 Intelsat C-band Satellites launched by SpaceX.
Automated and optimized weekly database installations of telemetry data using Bash scripts, Python, and unit tests, saving over 3 hours of work weekly.
Proposed and implemented persistent storage option, automatically uploading new telemetry information to physical data stores upon change."
		imageUrl="/employment/maxar.jpg"
		alt="Album"
		technologies={['Python', 'Bash', 'Shell']}
		buttons={[
			{
				text: 'Website',
				url: 'https://www.maxar.com/'
			}
		]}
	/>
</div>

<div class="flex w-full flex-col items-center gap-4 px-2 py-1">
	<EmploymentCard
		position="Research Assistant"
		company="Santa Cruz Institute for Particle Physics"
		date="March 2022 - June 2022"
		description="Collaborated on machine learning program with Professor Jason Nielsen and team to identify Higgs boson particle's correlating variables from sample size of over 200,000 events."
		imageUrl="/employment/scipp.jpg"
		alt="Album"
		technologies={['Python', 'Keras', 'TensorFlow', 'matplotlib', 'pandas', 'dBase', 'Jupyter Notebook']}
		buttons={[]}
	/>
</div>

<div class="divider m-0"></div>
<p class="m-2 text-center text-4xl">Education</p>

<div class="flex w-full flex-col px-2 py-1 lg:flex-row">
	<EmploymentCard
		position="Master of Science in Computer Science"
		company="UCLA"
		date="September 2023 - May 2025"
		description="Coursework includes software engineering, database systems/mining, artificial intelligence and life, and computer vision.
Social & Wellness Director for the UCLA Association of Indonesian Americans."
		imageUrl="/education/logo_UCLA_blue_boxed.png"
		alt="Album"
		technologies={[]}
		buttons={[]}
	/>

	<EmploymentCard
		position="Bachelor of Science in Computer Science"
		company="UCSC"
		date="July 2020 - June 2023"
		description="Summa Cum Laude, graduated with highest honors in major. Coursework includes database systems, computational models, analysis of algorithms, computer system design, computer architecture, and computer graphics."
		imageUrl="/education/logo_UCSC.jpg"
		alt="Album"
		technologies={[]}
		buttons={[]}
	/>
</div>
