<script lang="ts">
    import {scrollRef} from 'svelte-scrolling';

    export let sectionColour: string;
    export let sectionName: string;
</script>

<section use:scrollRef={sectionName} class="w-screen h-[120vh] lg:h-[60vh] flex lg:flex-col flex-row" style="background-color: {sectionColour};">
    <slot></slot>
</section>