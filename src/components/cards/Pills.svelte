<script>
    const skills = [
        "Python",
        "SQL",
        "Pandas",
        "Numpy",
        "SQL",
        "R programming",
        "Git",
        "GitHub",
        "IBM DB2",
        "Google Cloud platform",
        "Google analytics",
        "Tableau",
        "Excel",
        "Google Sheets",
        "MySQL",
        "PostgresSQL",
        "Jira",
        "Kanban",
        "Trello",
    ];

    const colors = [
        "slate",
        "neutral",
        "stone",
        "red",
        "orange",
        "amber",
        "yellow",
        "lime",
        "green",
        "emerald",
        "teal",
        "cyan",
        "sky",
        "blue",
        "indigo",
        "violet",
        "purple",
        "fuchsia",
        "pink",
        "rose",
    ];

    const randomSkill = skills[Math.floor(Math.random() * skills.length)];
    const color = colors[Math.floor(Math.random() * colors.length)];

    export let skill;
</script>

<div
    class={`border border-violet-200 bg-violet-100 rounded-full text-sm font-medium text-violet-500 py-2 px-6`}
>
    {skill}
</div>
