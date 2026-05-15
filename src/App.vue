<script setup>
import SectionAbout from "./components/SectionAbout.vue";
import SectionHero from "./components/SectionHero.vue";
import SectionProjCode from "./components/SectionProjCode.vue";
import SectionProjDesign from "./components/SectionProjDesign.vue";
import SectionSocial from "./components/SectionSocial.vue";
import SectionTech from "./components/SectionTech.vue";
import SectionThanks from "./components/SectionThanks.vue";
</script>

<template>
    <img
        class="hero-blur"
        src="./assets/images/background-blur.svg"
        role="presentation"
        alt=""
    />
    <main>
        <SectionHero></SectionHero>
        <SectionTech></SectionTech>
        <SectionProjCode></SectionProjCode>
        <SectionProjDesign></SectionProjDesign>
        <SectionAbout></SectionAbout>
        <SectionSocial></SectionSocial>
        <SectionThanks></SectionThanks>
    </main>
</template>

<style>
.hero-blur {
    width: 70vw;
    position: absolute;
    aspect-ratio: 1 / 1;
    top: -45vw;
    left: -20vw;
}
body {
    overflow-x: hidden;
}
</style>
