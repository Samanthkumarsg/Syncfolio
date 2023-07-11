<script>
    export let education;
</script>

<div
    class="border-s-2 border-dashed border-blue-300 flex flex-col justify justify-between p-8 py-6 group cursor-pointer"
>
    <div class="relative">
        <div class="flex flex-row items-center mb-3">
            <div
                class="h-3 w-3 rounded-full bg-blue-500 absolute -left-[2.4rem] group-hover:animate-pulse group-hover:bg-rose-500"
            />
            <div class="text-md font-semibold text-blue-500">
                {education.startDate}
            </div>
            <h1 class="mx-2">-</h1>
            <div class="text-md font-semibold text-blue-500">
                {education.endDate}
            </div>
        </div>
        <div class="flex flex-col">
            <h1 class="text-lg font-semibold mb-1 text-gray-900">
                {education.courseName}
            </h1>
            <h2 class="text-sm font-medium text-gray-500 normal-case">
                {education.collegeName}, {education.location}
            </h2>
        </div>
    </div>
</div>
