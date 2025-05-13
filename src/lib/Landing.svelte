<script lang='ts'>
    let { textToCopy }: { textToCopy: string } = $props();

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