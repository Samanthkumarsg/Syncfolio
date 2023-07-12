<script>
    import UserDetails from "./UserDetails.svelte";
    import Social from "./Social.svelte";
    import Summary from "./Summary.svelte";
    import GridColumnTwo from "./GridColumnTwo.svelte";
    import { portfolio } from "../store";
    import { onDestroy } from "svelte";

    let data = [];
    const unsubscribe = portfolio.subscribe((value) => {
        data = value;
        console.log(data);
    });

    onDestroy(() => unsubscribe());
</script>

<head>
    <meta property="og:title" content={data?.name} />
    <meta property="og:description" content={data?.summary} />

    <meta property="og:url" content="URL of your website" />
</head>

<div class="w-11/12 m-auto mt-16 rounded-2xl overflow-hidden">
    <UserDetails />
    <Social />
    <Summary />
    <GridColumnTwo />
</div>
