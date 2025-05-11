<script lang="ts">
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
				Hi! I'm a software engineer with professional experience in infrastructure, database
				management systems, system design, and configurations. I earned my master's degree in
				computer science from UCLA and graduated summa cum laude with a bachelor's degree in
				computer science from UCSC. Beyond work, I enjoy editing and filming videos, rock climbing,
				playing games, and collecting stuffed animals.
			</p>
			<button
				on:click={copyText}
				class="text-secondary-content btn btn-sm btn-ghost p-0 text-base underline"
			>
				williamwsantosa@gmail.com
				<img src="/clipboard.svg" alt="Copy" class="inline-block h-4 w-4" />
			</button>
			<div class="grid grid-flow-col">
				<button class="text-base-content btn btn-ghost text-lg px-0">
					<a href="mailto:williamwsantosa@gmail.com?subject=Lets connect!" target="_blank" rel="noopener noreferrer">
						<img src="/email.svg" alt="Email" class="inline-block h-8 w-8" />
					</a>
				</button>
				<button class="text-base-content btn btn-ghost text-lg px-1">
					<a href="https://www.linkedin.com/in/williamsantosa" target="_blank" rel="noopener noreferrer">
						<img src="/linkedin.svg" alt="LinkedIn" class="inline-block h-8 w-8" />
					</a>
				</button>
				<button class="text-base-content btn btn-ghost text-lg px-0">
					<a href="https://github.com/williamsantosa" target="_blank" rel="noopener noreferrer">
						<img src="/github.svg" alt="GitHub" class="inline-block h-8 w-8" />
					</a>
				</button>
			</div>
		</div>
		<div class="avatar">
			<div class="mask mask-squircle h-screen w-[90%]">
				<img src="/favicon.svg" alt="William Santosa Logo" />
			</div>
		</div>
	</div>
</div>

<div class="divider"></div>

<p>Hi</p>