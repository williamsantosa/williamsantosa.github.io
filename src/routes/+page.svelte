<script lang="ts">
	import Landing from '$lib/Landing.svelte';
	import SectionHeader from '$lib/SectionHeader.svelte';
	import EmptyCard from '$lib/EmptyCard.svelte';
	import ProjectCard from '$lib/ProjectCard.svelte';
	import EmploymentCard from '$lib/EmploymentCard.svelte';
	import SectionHeaderSplit from '$lib/SectionHeaderSplit.svelte';	
</script>

<Landing textToCopy='williamwsantosa@gmail.com'/>

<SectionHeaderSplit title_left="Now" title_right="Building" />

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
		title="Studio Management Application v2"
		date="July 2025 - Present"
		description=""
		imageUrl="/projects/placeholder.svg"
		alt="Placeholder Image"
		technologies={[]}
		buttons={[]}
	/>
</div>

<SectionHeader title="Projects" />

<div class="flex w-full flex-col px-2 py-1 lg:flex-row">
	<ProjectCard
		title="Last of Sus: Zombie Apocalypse Simulation"
		date="April 2024 - June 2024"
		description="Artificlal Life Zombie Apocalypse Simulation written in Unity utililizing boid behavior, behavior trees, L systems, A star algorithm, raytracing, and more."
		imageUrl="/projects/lastofsus.gif"
		alt="Simulation wwith zombies, l systems, and boids"
		technologies={['Unity', 'C#']}
		buttons={[
			{
				text: 'Report',
				url: 'https://github.com/williamsantosa/williamsantosa/blob/main/Misc/CS_275_S24_Report.pdf'
			},
			{
				text: 'Code',
				url: 'https://github.com/Last-of-sus/main/tree/main'
			}
		]}
	/>

	<ProjectCard
		title="Hand Cropper"
		date="May 2024 - June 2024"
		description="Real-time hand cropper using active contour snakes, convex-hull algorithm, and various other optimization techniques."
		imageUrl="/projects/handcropper.gif"
		alt="Hand cropper application in action"
		technologies={['Python', 'MediaPipe', 'OpenCV', 'Matplotlib']}
		buttons={[
			{
				text: 'Report',
				url: 'https://github.com/williamsantosa/williamsantosa/blob/main/Misc/CS_269_S24_Report.pdf'
			},
			{
				text: 'Code',
				url: 'https://github.com/williamsantosa/Not-Clash-v2'
			}
		]}
	/>

	<ProjectCard
		title="Inverse Kinematics Human"
		date="February 2024 - March 2024"
		description="Simulation of a human arm tracing on a blackboard using inverse kinematics with Jacobian-based methods and kinematic modeling."
		imageUrl="/projects/ikhuman.gif"
		alt="Articulated human model tracing a path on blackboard"
		technologies={['JavaScript', 'Node.js', 'Three.js', 'WebGL']}
		buttons={[
			{
				text: 'Code',
				url: 'https://github.com/williamsantosa/CS174C-Assignment2'
			}
		]}
	/>
</div>

<div class="flex w-full flex-col px-2 py-1 lg:flex-row">
	<ProjectCard
		title="NoteScript"
		date="February 2023"
		description="Full stack web application that generate notes from transcripts."
		imageUrl="/projects/notescript.png"
		alt="Front Page"
		technologies={['JavaScript', 'Node.js', 'Flask', 'OpenAI API']}
		buttons={[
			{
				text: 'Code',
				url: 'https://github.com/williamsantosa/TFC-Boston-Hackathon-2023'
			}
		]}
	/>

	<ProjectCard
		title="Not Clash v2"
		date="January 2023"
		description="Second iteration of the original Not Clash discord bot. Facilitates League of Legends matches, stores player and match information in SQLite database, and provides concurrent matchmaking based off Elo rating with many players."
		imageUrl="/projects/reksai.jpeg"
		alt="Primordian Rek'Sai Splash Art"
		technologies={['JavaScript', 'Node.js', 'SQLite', 'Discord.js']}
		buttons={[
			{
				text: 'Code',
				url: 'https://github.com/williamsantosa/Not-Clash-v2'
			}
		]}
	/>

	<ProjectCard
		title="A Guide to the UCSC's CS Majors"
		date="January 2023 - March 2023"
		description="Collaborated in a team of three to create a guide to UCSC's Bachelor of Science/Arts in Computer Science and Bachelor of Science in Computer Science: Computer Game Design majors. Contains descriptions of courses, programming languages, professors, and graduation requirements."
		imageUrl="/projects/ucsc_campus.jpg"
		alt="Campus Image"
		technologies={[]}
		buttons={[
			{
				text: 'Code',
				url: 'https://github.com/williamsantosa/ucsc-cs'
			}
		]}
	/>
</div>

<div class="flex w-full flex-col px-2 py-1 lg:flex-row">
	<EmptyCard />
	<ProjectCard
		title="YouToo"
		date="August 2022 - September 2022"
		description="Desktop application for fast and convenient downloading of YouTube videos for offline access."
		imageUrl="/projects/youtube.png"
		alt="YouTube Logo"
		technologies={['Python', 'PyQt6', 'PyTube']}
		buttons={[
			{
				text: 'Code',
				url: 'https://github.com/williamsantosa/YouToo'
			}
		]}
	/>
	<EmptyCard />
</div>

<SectionHeader title="Employment" />

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
		description="Developed internal features for Intelsat’s Galaxy-31 and Galaxy-32 C-band satellites launched by SpaceX. Automated weekly telemetry database installs with Bash and Python, saving 3+ hours per week. Proposed and implemented persistent storage to auto-upload updated telemetry data."
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
		description="Collaborated with Professor Jason Nielsen and team on a machine learning project to identify variables correlated with the Higgs boson from 200,000+ particle collision events."
		imageUrl="/employment/scipp.jpg"
		alt="Album"
		technologies={[
			'Python',
			'Keras',
			'TensorFlow',
			'matplotlib',
			'pandas',
			'dBase',
			'Jupyter Notebook'
		]}
		buttons={[
			{
				text: 'Website',
				url: 'https://scipp.science.ucsc.edu/'
			}
		]}
	/>
</div>

<SectionHeader title="Education" />

<div class="flex w-full flex-col px-2 py-1 lg:flex-row">
	<EmploymentCard
		position="Master of Science in Computer Science"
		company="UCLA"
		date="September 2023 - May 2025"
		description="Coursework includes software engineering, database systems/mining, artificial intelligence and life, and computer vision.
Served as the Social & Wellness Director for the UCLA Association of Indonesian Americans during the 2024 school year."
		imageUrl="/education/logo_UCLA_blue_boxed.png"
		alt="Album"
		technologies={[]}
		buttons={[
			{
				text: 'Degree',
				url: 'https://grad.ucla.edu/programs/computer-science/'
			},
			{
				text: 'Website',
				url: 'https://www.ucla.edu/'
			}
		]}
	/>

	<EmploymentCard
		position="Bachelor of Science in Computer Science"
		company="UCSC"
		date="July 2020 - June 2023"
		description="Graduated summa cum laude with highest honors in major. Coursework includes database systems, computational models, analysis of algorithms, computer system design, computer architecture, and computer graphics."
		imageUrl="/education/logo_UCSC.jpg"
		alt="Album"
		technologies={[]}
		buttons={[
			{
				text: 'Degree',
				url: 'https://bpb-us-w2.wpmucdn.com/wordpress.ucsc.edu/dist/2/88/files/2023/09/CS_BS_20-21-1.pdf'
			},
			{
				text: 'Website',
				url: 'https://www.ucsc.edu/'
			}
		]}
	/>
</div>
