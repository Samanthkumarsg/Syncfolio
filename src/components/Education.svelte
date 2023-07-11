<script>
    import { onDestroy } from "svelte";
    import { portfolio } from "../store";
    import RoadmapCard from "./cards/RoadmapCard.svelte";

    let educationDetails = [];

    const unsubscribe = portfolio.subscribe((value) => {
        educationDetails = value?.contents?.education;
    });

    onDestroy(() => {
        unsubscribe();
    });
</script>

<div
    class="grid sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-1 xl:grid-cols-1 gap-8"
>
    <div
        class="border rounded-2xl p-8 sm:p-8 md:p-10 lg:p-10 xl:p-10 bg-white shadow-sm h-fit"
    >
        <h1 class="text-lg font-bold text-gray-800 mb-6">Education</h1>
        {#each educationDetails as education}
            <RoadmapCard {education} />
        {/each}
    </div>
</div>
