<script lang="ts">
    import { scrollTo } from 'svelte-scrolling';

    let y = 0;
    let windowHeight = 0;
</script>

<div class="flex flex-col">
    <div class="text-white w-screen bg-[#013C58] h-[70vh] z-50 top-0 flex lg:flex-row flex-col justify-start items-center">
        <div class="flex flex-col p-20">
            <h1 class="py-6 text-[4rem]">Corey Sutcliffe</h1>
            <br/>
            <h2 class="text-3xl">Frontend developer & web designer</h2>
            <h2 class="text-3xl">Work in Progress CV site</h2>
        </div>
    </div>
    <div class="bg-[#013C58] h-[10vh] flex items-center justify-center">
        <div use:scrollTo={'Skills'} class="h-[48px] w-[48px]">
            <svg class="animate-bounce" xmlns="http://www.w3.org/2000/svg" height="48" width="48"><path fill="#fff" d="M24 40 8 24l2.1-2.1 12.4 12.4V8h3v26.3l12.4-12.4L40 24Z"/></svg>
        </div>
    </div>
</div>
{#if y > (windowHeight * 0.65)}
<div class="text-white w-screen bg-[#013C58] top-0 h-16 fixed z-50 flex items-center">
    <p class="text-3xl m-4">Corey Sutcliffe</p>
</div>
{/if}

<svelte:window  bind:scrollY={y} bind:outerHeight={windowHeight}/>