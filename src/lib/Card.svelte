<script lang="ts">
    export let cardTitle: string;
    export let cardImage: string;
</script>

<div class=" flex justify-center flex-col items-center w-72 lg:w-96">
    <div>
        <img class="h-28 lg:h-44 w-auto" src={cardImage} alt={cardTitle}/>
    </div>
    <h1 class="text-3xl">{cardTitle}</h1>
    <slot/>
</div>