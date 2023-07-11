<script>
    import ProjectsCard from "./cards/ProjectsCard.svelte";
    import { portfolio } from "../store";
    import { onDestroy } from "svelte";

    let projects = [];
    const unsubscribe = portfolio.subscribe((value) => {
        projects = value?.contents?.projects;
    });

    onDestroy(() => {
        unsubscribe();
    });
</script>

<div
    class="border rounded-2xl p-8 sm:p-8 md:p-10 lg:p-10 xl:p-10 bg-white shadow-sm h-fit"
>
    <h1 class="text-lg font-bold text-gray-800 mb-6">Projects</h1>
    {#each projects as project}
        <ProjectsCard {project} />
    {/each}
</div>
