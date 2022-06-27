<script lang="ts">
    export let sectionColour: string;
</script>

<section class="w-screen h-[60vh]" style="background-color: {sectionColour};">
    <slot></slot>
</section>