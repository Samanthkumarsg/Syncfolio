<script>
    import Education from "./Education.svelte";
    import Experience from "./Experience.svelte";
    import Projects from "./Projects.svelte";
    import Skills from "./Skills.svelte";
</script>

<div class="my-8 rounded-xl grid sm:grid-cols-1 lg:grid-cols-2 gap-8">
    <div
        class="grid sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-1 xl:grid-cols-1 gap-8"
    >
        <!--  -->
        <Experience />
        <Education />
        <!--  -->
    </div>

    <div
        class=" grid sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-1 xl:grid-cols-1 gap-8 self-start"
    >
        <!--  -->
        <Skills />
        <Projects />
    </div>
</div>
