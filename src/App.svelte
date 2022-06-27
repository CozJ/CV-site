<script lang="ts">
  //import "./app.css";
  import Hero from "./lib/Hero.svelte";
  import Section from "./lib/Section.svelte";
  import WaveDivider from "./lib/WaveDivider.svelte";
</script>

<svelte:head>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Ubuntu&display=swap');

    @tailwind base;
    @tailwind components;
    @tailwind utilities;

    body {
      font-family: 'Ubuntu', sans-serif;
    }
  </style>
</svelte:head>

<main class="overflow-x-hidden">
  <Hero/>
  <Section sectionColour={"#fff"}>
    <div class="w-[100%] h-[100%] flex">
      
    </div>
  </Section>
  <WaveDivider waveColour={"#e3941e"} invert={false}/>
  <Section sectionColour={"#e3941e"}>
    <div class="w-[100%] h-[100%] flex">

    </div>
  </Section>
  <WaveDivider waveColour={"#e3941e"} invert={true}/>
</main>