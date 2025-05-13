<script lang="ts">
    let {
        title_left,
        title_right
    }: {
        title_left: string;
        title_right: string;
    } = $props();
</script>

<div class="divider m-0"></div>
<div class="flex w-full flex-col px-2 py-1 lg:flex-row">
	<div class="w-full p-2 lg:w-1/2">
		<p class="m-2 text-center text-4xl">{title_left}</p>
	</div>
	<div class="w-full p-2 lg:w-1/2">
		<p class="m-2 hidden text-center text-4xl lg:block">{title_right}</p>
	</div>
</div>