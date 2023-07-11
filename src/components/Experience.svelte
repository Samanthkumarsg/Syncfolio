<script>
    import { onDestroy } from "svelte";
    import { portfolio } from "../store";
    import ExperienceCard from "./cards/ExperienceCard.svelte";

    let experienceDetails = [];

    const unsubscribe = portfolio.subscribe((value) => {
        experienceDetails = value?.contents?.work_experience;
    });

    onDestroy(() => {
        unsubscribe();
    });
</script>

<div
    class="border rounded-2xl p-8 sm:p-8 md:p-10 lg:p-10 xl:p-10 mb-8 bg-white shadow-sm h-fit"
>
    <h1 class="text-lg font-bold text-gray-800 mb-6">Experience</h1>
    {#each experienceDetails as experience}
        <ExperienceCard {experience} />
    {/each}
</div>
