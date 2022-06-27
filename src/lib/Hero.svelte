<script lang="ts">
    import selfie from "/src/assets/selfie.png";

    let y = 0;
    let windowHeight = 0;
</script>

<div class="text-white w-screen bg-[#013C58] h-[80vh] z-50 shadow-lg top-0 flex lg:flex-row flex-col justify-around items-center">
    <div class="text-[3rem] flex flex-col">
        <h1>Corey Sutcliffe</h1>

    </div>
    <img class="h-[50vh] w-auto aspect-auto rounded-[50%]" src="{selfie}" alt="selfie"/>
</div>
{#if y > (windowHeight * 0.70)}
<div class="text-white w-screen bg-[#013C58] shadow-lg top-0 fixed z-50 flex items-center">
    <p class="text-3xl m-4">Corey Sutcliffe</p>
</div>
{/if}

<svelte:window  bind:scrollY={y} bind:outerHeight={windowHeight}/>