<script lang="ts">
    import { scrollTo } from 'svelte-scrolling';
    import Menu from "svelte-material-icons/Menu.svelte";
    import MenuOpen from "svelte-material-icons/MenuOpen.svelte";

    let open: boolean = false;

    export let y: number = 0;

    function OnClick () {
        open = !open;
    }
</script>

<div class="text-white min-w-full max-w-full bg-[#013C58] top-0 fixed h-16 z-50 flex flex-row items-center justify-between">
    <p class="text-3xl m-4">Corey Sutcliffe {y}</p>
    {#if open == true}
    <div class="pr-4" on:click={OnClick}>
        <MenuOpen color="white" height="48" width="48"/>
    </div>
    <!-- <ul class="text-2xl flex flex-row">
        <li use:scrollTo={'Skills'} class="m-4">Skills</li>
        <li use:scrollTo={'Workplace'} class="m-4">WorkPlace</li>
        <li use:scrollTo={'Projects'} class="m-4">Projects</li>
    </ul> -->
    {:else if open == false}
    <div class="pr-4" on:click={OnClick}>
        <Menu color="white" height="48" width="48"/>
    </div>
    {/if}
</div>