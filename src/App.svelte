<script lang="ts">
  //import "./app.css";
  import Hero from "./lib/Hero.svelte";
  import Section from "./lib/Section.svelte";
  import WaveDivider from "./lib/WaveDivider.svelte";
  import Card from "./lib/Card.svelte";
  import SvelteLogo from "./assets/svelte-logo.png";
  import ReactLogo from "./assets/react-logo.png";
  import BlazorLogo from "./assets/blazor-logo.png";
  import DotNetLogo from "./assets/NET-logo.svg";
</script>

<svelte:head>
  <style>
    @import url("https://fonts.googleapis.com/css2?family=Ubuntu&display=swap");

    @tailwind base;
    @tailwind components;
    @tailwind utilities;

    body {
      font-family: "Ubuntu", sans-serif;
    }
  </style>
</svelte:head>


<main>
  <Hero />
  <Section sectionColour={"#fff"} sectionName="Skills">
    <h1 class="text-3xl m-4 lg:m-20 font-bold">Frameworks Used</h1>
    <div class="w-screen max-w-full flex flex-col lg:flex-row justify-around items-center">
      <Card cardTitle="Svelte" cardImage={SvelteLogo} TimeUsed="2022 - Current">
        <p class="text-2xl pt-2 text-center">
          The latest Framework I have taken to using for setting up quick and
           easy Component based reactive sites.
        </p>
      </Card>
      <Card cardTitle="React" cardImage={ReactLogo} TimeUsed="2021 - Current">
        <p class="text-2xl pt-2 text-center">
          React a powerfull and customisable Framework I have used 
          within a profesional setting for work. 
        </p>
      </Card>
      <Card cardTitle='.NET' cardImage={DotNetLogo} TimeUsed="2020 - 2021">
        <p class="text-2xl pt-2 text-center">
          Framework I used in my second year at University for the
          module 'Modern Web Development'.
        </p>
      </Card>
    </div>
  </Section>
  <WaveDivider waveColour={"#e3941e"} invert={false} />
  <Section sectionColour={"#e3941e"} sectionName="Workplace">
    <div class="w-[100%] h-[100%] flex" />
  </Section>
  <WaveDivider waveColour={"#e3941e"} invert={true} />
  <Section sectionColour={"#fff"} sectionName="Projects">
    <div class="w-[100%] h-[100%] flex" />
  </Section>
</main>
