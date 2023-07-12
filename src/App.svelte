<script>
  import { onMount } from "svelte";
  import Layoult from "./components/__Layoult.svelte";
  import { portfolio } from "./store";
  import jsonData from "./data.json";

  portfolio.set(jsonData);
</script>

<div>
  <Layoult />
</div>
