<script lang="ts">
	let {
		position,
		company,
		date,
		description,
		imageUrl,
        alt,
        technologies,
		buttons
	}: {
		position: string;
		company: string;
		date: string;
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

<div class="w-full p-2 md:w-full lg:w-1/2">
	<div class="card lg:card-side bg-base-200 shadow-sm justify-start w-full h-full">
		<figure class="flex-shrink-0 md:h-[400px] lg:w-[45%] w-60% w-full h-full">
			<img
				src={imageUrl}
				alt={alt}
				class="object-cover"
			/>
		</figure>
		<div class="card-body">
			<h2 class="card-title">{`${position} · ${company}`}</h2>
			<p class="text-sm">{date}</p>
			<p class="">{description}</p>
            <div class="flex flex-wrap gap-2">
                {#each technologies as technology}
                    <span class="badge badge-outline">{technology}</span>
                {/each}
            </div>
			<div class="flex flex-wrap h-full"></div> <!-- Added to keep all the elements at the top of card lol -->
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
