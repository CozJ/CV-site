<script lang="ts">
  //import "./app.css";
  import Hero from "./lib/Hero.svelte";
  import Section from "./lib/Section.svelte";
  import WaveDivider from "./lib/WaveDivider.svelte";
  import Card from "./lib/Card.svelte";
  import SvelteLogo from "./assets/svelte-logo.png";
  import ReactLogo from "./assets/react-logo.png";
  import BlazorLogo from "./assets/blazor-logo.png";

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
  <Section sectionColour={"#fff"} sectionName='Skills'>
    <h1 class="text-3xl m-4 lg:m-16 font-bold">Frameworks Used</h1>
    <div class="w-screen flex flex-col lg:flex-row justify-around items-center">
      <Card cardTitle="Svelte" cardImage={SvelteLogo}>
        <p class="text-2xl">Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem est veniam harum iste. Quisquam, neque ducimus.</p>
      </Card>
      <Card cardTitle="React" cardImage={ReactLogo}>
        <p class="text-2xl">Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem est veniam harum iste. Quisquam, neque ducimus.</p>
      </Card>
      <Card cardTitle="Blazor" cardImage={BlazorLogo}>
        <p class="text-2xl">Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem est veniam harum iste. Quisquam, neque ducimus.</p>
      </Card>
    </div>
  </Section>
  <WaveDivider waveColour={"#e3941e"} invert={false}/>
  <Section sectionColour={"#e3941e"} sectionName='Workplace'>
    <div class="w-[100%] h-[100%] flex">

    </div>
  </Section>
  <WaveDivider waveColour={"#e3941e"} invert={true}/>
  <Section sectionColour={"#fff"} sectionName='Projects'>
    <div class="w-[100%] h-[100%] flex">

    </div>
  </Section>
</main>