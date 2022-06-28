<script lang="ts">
    import {scrollRef} from 'svelte-scrolling';

    export let sectionColour: string;
    export let sectionName: string;
</script>

<section use:scrollRef={sectionName} class="w-screen h-[160vh] lg:h-[60vh] flex flex-col" style="background-color: {sectionColour};">
    <slot></slot>
</section>