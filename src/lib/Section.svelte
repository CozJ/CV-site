<script lang="ts">
    import {scrollRef} from 'svelte-scrolling';

    export let sectionColour: string;
    export let sectionName: string;
    export let TimeUsed: string = null;
</script>

<section use:scrollRef={sectionName} class="min-w-full max-w-full h-[160vh] lg:h-[70vh] flex flex-col" style="background-color: {sectionColour};">
    {#if (TimeUsed != null)}
    <h5>Used From:{TimeUsed}</h5>
    {/if}
    <slot></slot>
</section>