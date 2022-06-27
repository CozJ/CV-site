<script lang="ts">
    import selfie from "/src/assets/selfie.png";

    let y = 0;
</script>

<div class="w-screen bg-[#013C58] h-[80vh] z-50 shadow-lg top-0 flex">
    <div>
        <p>hello</p>
    </div>
    <img class="h-40" src="{selfie}" alt="selfie"/>
</div>
{#if y > 585}
<div class="w-screen bg-[#013C58] shadow-lg top-0 fixed z-50 flex items-center">
    <p class="text-white text-3xl m-4">Corey Sutcliffe</p>
</div>
{/if}

<svelte:window  bind:scrollY={y}/>