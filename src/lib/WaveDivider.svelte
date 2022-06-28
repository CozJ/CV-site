<script lang="ts">
    export let waveColour: string;
    export let invert: boolean;
    let width: number;
</script>

{#if invert == false}
    <svg xmlns="http://www.w3.org/2000/svg" width="{width}" viewBox="0 0 1440 310"><path fill="{waveColour}" fill-opacity="1" d="M0,224L60,234.7C120,245,240,267,360,272C480,277,600,267,720,240C840,213,960,171,1080,149.3C1200,128,1320,128,1380,128L1440,128L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"></path></svg>
{:else if invert == true}
    <svg style="transform: scaleY(-1) scaleX(-1);" width="{width}" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 310"><path fill="{waveColour}" fill-opacity="1" d="M0,224L60,234.7C120,245,240,267,360,272C480,277,600,267,720,240C840,213,960,171,1080,149.3C1200,128,1320,128,1380,128L1440,128L1440,320L1380,320C1320,320,1200,320,1080,320C960,320,840,320,720,320C600,320,480,320,360,320C240,320,120,320,60,320L0,320Z"></path></svg>
{/if}

<svelte:window bind:innerWidth={width}></svelte:window>
