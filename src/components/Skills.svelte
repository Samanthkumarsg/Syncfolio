<script>
    import { onDestroy } from "svelte";
    import { portfolio } from "../store";
    import Pills from "./cards/Pills.svelte";

    let skills = [];

    const unsubscribe = portfolio.subscribe((value) => {
        skills = value?.contents?.skills?.skills;
        console.log(skills);
    });

    onDestroy(() => {
        unsubscribe();
    });
</script>

<div
    class="border rounded-2xl p-8 sm:p-8 md:p-10 lg:p-10 xl:p-10 bg-white h-fit shadow-sm cursor-pointer"
>
    <h1 class="text-lg font-bold text-gray-800 mb-6">Skills</h1>
    <div class="flex flex-wrap gap-4">
        {#each skills as skill}
        <Pills {skill}/>
            
        {/each}
    </div>
</div>
