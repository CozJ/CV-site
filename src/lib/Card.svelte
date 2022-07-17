<script lang="ts">
    export let cardTitle: string;
    export let cardImage: string;
    export let TimeUsed: string = null;
</script>

<div class=" flex justify-center flex-col items-center w-64 lg:w-80">
    <div>
        <img class="h-28 lg:h-44 w-auto" src={cardImage} alt={cardTitle}/>
    </div>
    <h1 class="text-3xl font-bold">{cardTitle}</h1>
    {#if (TimeUsed != null)}
    <h5 class="text-xl">Used From: {TimeUsed}</h5>
    {/if}
    <slot/>
</div>