<script>
    import Cell from "./cell.svelte";
    export let cellCount = [1, 2, 3, 4, 5];
    export let rowCount = [1, 2, 3];
</script>

<div class="header row">
    {#each cellCount as cell}
        <Cell class="header"></Cell>
    {/each}
</div>
{#each rowCount as row}
    <div class="row">
        {#each cellCount as cell}
            <Cell></Cell>
        {/each}
    </div>
{/each}

<style>
    .row {
        display: flex;
        flex-direction: row;
    }
    .header {
        border-bottom: 1px solid black;
    }
    .header {
        background-color: white;
    }
</style>