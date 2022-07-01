<script lang="ts">
    import { scrollTo } from 'svelte-scrolling';

    let y = 0;
    let windowHeight = 0;
    let windowWidth = 0;
</script>

<div class="flex flex-col bg-[#013C58]">
    <div class="text-white w-screen max-w-full h-[90vh] z-50 top-0 flex lg:flex-row flex-col justify-start items-center">
        <div class="flex flex-col p-10 lg:p-20 max-w-full lg:w-1/2">
            <h1 class="py-6 text-[4rem] font-bold">Corey Sutcliffe</h1>
            <br/>
            <h2 class="text-3xl">Frontend developer & web designer</h2>
            <h2 class="text-3xl">Work in Progress CV site</h2>
        </div>
        <div class="flex flex-col p-10 lg:p-20 invisible lg:visible max-w-full lg:w-1/2">
            <p>Hello how are you</p>
        </div>
    </div>
    <div class="h-[10vh] flex items-center justify-center">
        <div use:scrollTo={'Skills'}  class="h-[48px] w-[48px] animate-bounce">
            <svg style="filter: drop-shadow(3px 5px 2px rgb(0 0 0 / 0.4)); transform: scaleY(1.5) scaleX(1.5);" xmlns="http://www.w3.org/2000/svg" height="48" width="48"><path fill="#fff" d="M24 38 12 26l2.1-2.1 9.9 9.9 9.9-9.9L36 26Zm0-12.65-12-12 2.1-2.1 9.9 9.9 9.9-9.9 2.1 2.1Z"/></svg>
        </div>
    </div>
</div>
{#if y > (windowHeight * 0.65)}
<div class="text-white min-w-full max-w-full bg-[#013C58] top-0 fixed h-16 z-50 flex flex-row items-center justify-between">
    <p class="text-3xl m-4">Corey Sutcliffe</p>
    <ul class="text-2xl flex flex-row">
        <li use:scrollTo={'Skills'} class="m-4">Skills</li>
        <li use:scrollTo={'Workplace'} class="m-4">WorkPlace</li>
        <li use:scrollTo={'Projects'} class="m-4">Projects</li>
    </ul>
</div>
{/if}

<svelte:window  bind:scrollY={y} bind:outerHeight={windowHeight} bind:outerWidth={windowWidth}/>