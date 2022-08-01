<script lang="ts">
    import { scrollTo } from 'svelte-scrolling';
    import Navbar from "./Navbar.svelte";
    import KeyboardDoubleArrowDown from "svelte-material-icons/ChevronDoubleDown.svelte";
    import ThreeContainer from "./ThreeContainer.svelte";

    let y: number = 0;
    let windowHeight: number = 0;
    let windowWidth: number = 0;
</script>

<div class="flex flex-col bg-[#013C58]">
    <div class="text-white w-screen max-w-full h-[90vh] z-50 top-0 flex lg:flex-row flex-col justify-start items-center">
        <div class="flex flex-col p-10 lg:p-20 max-w-full lg:w-1/2">
            <h1 class="py-6 text-[3.5rem] lg:text-[4rem] font-bold">Corey Sutcliffe</h1>
            <br/>
            <h2 class="leading-loose text-xl lg:text-3xl">Sheffield Hallam University</h2>
            <h2 class="leading-loose text-xl lg:text-3xl">Student & Frontend developer</h2>
            <h2 class="leading-loose text-xl lg:text-3xl">Work in Progress CV site</h2>
        </div>
        <div class="flex flex-col p-10 lg:p-20 max-w-full lg:w-1/2">
            <ThreeContainer/>
        </div>
    </div>
    <div class="h-[10vh] flex items-center justify-center">
        <div use:scrollTo={'Skills'}  class="h-[48px] w-[48px] animate-bounce">
            <KeyboardDoubleArrowDown color="white" height="64" width="64"/>
        </div>
    </div>
</div>
{#if y > (windowHeight * 0.85)}
    <Navbar ></Navbar>
{/if}

<svelte:window  bind:scrollY={y} bind:outerHeight={windowHeight} bind:outerWidth={windowWidth}/>