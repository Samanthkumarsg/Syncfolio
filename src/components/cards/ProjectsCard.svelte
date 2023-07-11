<script>
    export let project;
    console.log(project);
</script>

<div
    class=" border-2 border-dashed border-blue-300 border-spacing-4 rounded-2xl flex flex-col justify justify-between p-8 mb-8 hover:border-blue-500 cursor-pointer"
>
    <div class="relative">
        <div class="flex flex-row flex-wrap items-center mb-4 gap-3">
            {#each project.toolsUsed as item}
                <div
                    class="text-xs bg-blue-100 px-4 py-2 border border-blue-200 font-semibold rounded-md text-blue-500"
                >
                    {item}
                </div>
            {/each}
        </div>
        <!--  -->
        <hr class="my-5" />

        <div class="flex flex-col">
            <h1 class="text-lg font-semibold mb-3 text-gray-900">
                {project.title}
            </h1>
            <h2 class="text-sm font-medium text-gray-500 normal-case">
                {project.description}
            </h2>
            <hr class="my-5" />
            <a
                href={project.url}
                class="text-sm bg-blue-500 text-white px-6 py-2 w-fit rounded-lg"
                >View project</a
            >
        </div>
    </div>
</div>
