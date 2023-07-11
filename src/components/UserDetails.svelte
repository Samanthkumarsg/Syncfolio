<script>
    import { portfolio } from "../store";

    console.log(portfolio);
</script>

<div class="flex p-10 pb-5 bg-white sticky top-0">
    <div class=" w-full flex flex-col flex-wrap">
        <h1 class="text-2xl font-semibold text-blue-500">
            {$portfolio?.name}
        </h1>
        <h2 class="text-md font-medium text-gray-400 mt-2">
            {$portfolio?.role}
        </h2>

        <!-- contact details -->
        <!-- <div class="my-3 flex flex-row flex-wrap gap-4">
            <h6 class="text-gray-400 text-sm">+49 17632308662</h6>
            <h6 class="text-gray-400 text-sm">+49 17632308662</h6>
        </div> -->
    </div>
</div>
