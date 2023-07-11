<script>
    export let experience;
    let {
        start_date,
        end_date,
        company,
        location,
        position,
        responsibilities,
    } = experience;
</script>

<div
    class="border-2 border-dashed border-blue-300 border-spacing-4 rounded-2xl flex flex-col justify justify-between p-8 mb-8 hover:border-blue-500 cursor-pointer"
>
    <div class="relative">
        <div class="flex flex-row items-center mb-3">
            <div class="text-md font-semibold text-blue-500">
                {start_date}
            </div>
            <h1 class="mx-2">-</h1>
            <div class="text-md font-semibold text-blue-500">{end_date}</div>
        </div>
        <div class="flex flex-col">
            <h1 class="text-lg font-semibold mb-1 text-gray-900">
                {position}
            </h1>
            <h2 class="text-sm font-medium text-gray-500 normal-case">
                {company}, {location}
            </h2>
            <hr class="my-6" />
            <ul class="list-disc list-outside leading-normal mt-3 pl-4">
                {#each responsibilities as responsibility}
                    <li class="text-gray-700 font-medium mb-3">
                        {responsibility}
                    </li>
                {/each}
            </ul>
        </div>
    </div>
</div>
