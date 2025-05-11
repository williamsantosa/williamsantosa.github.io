<script lang="ts">
	let {
		title,
		description,
		imageUrl,
        alt,
        technologies,
		buttons
	}: {
		title: string;
		description: string;
		imageUrl: string;
        alt: string;
        technologies: Array<string>;
		buttons: Array<{
            text: string;
            url: string;
        }>;
	} = $props();
</script>

<div class="w-full p-2 md:w-1/2">
	<div class="card lg:card-side bg-base-200 shadow-sm justify-start w-full h-full">
		<figure class="flex-shrink-0 md:h-[400px] md:w-[45%] w-full h-full overflow-hidden">
			<img
				src={imageUrl}
				alt={alt}
				class="object-cover"
			/>
		</figure>
		<div class="card-body">
			<h2 class="card-title">{title}</h2>
			<p class="">{description}</p>
            <div class="flex flex-wrap gap-2 h-full">
                {#each technologies as technology}
                    <span class="badge badge-outline">{technology}</span>
                {/each}
            </div>
			<div class="card-actions justify-end">
                {#each buttons as button}
                    <button class="btn btn-primary">
                        <a href={button.url} target="_blank" rel="noopener noreferrer">{button.text}</a>
                    </button>
                {/each}
			</div>
		</div>
	</div>
</div>
