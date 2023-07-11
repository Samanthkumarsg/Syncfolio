<script>
    import UserDetails from "./UserDetails.svelte";
    import Social from "./Social.svelte";
    import Summary from "./Summary.svelte";
    import GridColumnTwo from "./GridColumnTwo.svelte";
    import { portfolio } from "../store";
</script>

<div class="w-11/12 m-auto mt-16 rounded-2xl overflow-hidden">
    <UserDetails />
    <Social />
    <Summary />
    <GridColumnTwo />
</div>
