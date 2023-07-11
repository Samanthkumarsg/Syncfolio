<script>
    import { portfolio } from "../store";

    const { portfolioPage, github, linkedIn, instagram, facebook, dribble } =
        $portfolio.links;
</script>

<!-- Social buttons -->
<div
    class="p-8 sm:p-8 md:p-10 lg:p-10 xl:p-10 flex flex-row flex-wrap border-t-2 border-dashed py-6 gap-3 bg-white"
>
    <a
        href={portfolioPage}
        target="_blank"
        class="bg-blue-100 text-sm px-4 py-2 text-blue-500 rounded-lg border border-blue-200 hover:border-blue-500"
    >
        Portfolio
    </a>
    <a
        href={github}
        target="_blank"
        class="bg-blue-100 text-sm px-4 py-2 text-blue-500 rounded-lg border border-blue-200 hover:border-blue-500"
        >Github
    </a>
    <a
        href={instagram}
        target="_blank"
        class="bg-blue-100 text-sm px-4 py-2 text-blue-500 rounded-lg border border-blue-200 hover:border-blue-500"
        >Instagram
    </a>
    <a
        href={facebook}
        target="_blank"
        class="bg-blue-100 text-sm px-4 py-2 text-blue-500 rounded-lg border border-blue-200 hover:border-blue-500"
        >Facebook
    </a>

    <a
        href={dribble}
        target="_blank"
        class="bg-blue-100 text-sm px-4 py-2 text-blue-500 rounded-lg border border-blue-200 hover:border-blue-500"
        >Dribble
    </a>
    <a
        href={$portfolio.email}
        target="_blank"
        class="bg-blue-100 text-sm px-4 py-2 text-blue-500 rounded-lg border border-blue-200 hover:border-blue-500"
        >Email
    </a>
</div>
