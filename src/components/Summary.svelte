<script>
    import { onDestroy } from "svelte";
    import { portfolio } from "../store";

    let Summary = [];

    const unsubscribe = portfolio.subscribe((value) => {
        Summary = value?.summary;
        console.log(Summary);
    });

    onDestroy(() => {
        unsubscribe();
    });
</script>

<div
    class="border-t-2 border-dashed p-8 sm:p-8 md:p-10 lg:p-10 xl:p-10 flex-col bg-white"
>
    <h1 class="text-gray-800 font-bold text-lg mb-3">Summary</h1>
    <p class="text-md text-gray-700 leading-relaxed font-medium">
        {Summary}
    </p>
</div>
