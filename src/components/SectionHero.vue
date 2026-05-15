<script setup>
import Title from "./Title.vue";
import ButtonPrimary from "./ButtonPrimary.vue";
import ButtonSecondary from "./ButtonSecondary.vue";
import Instagram from "../assets/images/social/social-instagram.svg";

const link_matrix =
    "https://matrix.to/#/@igorfmoraes:matrix.org?client=im.fluffychat";
</script>
<template>
    <section id="hero">
        <span aria-hidden="true"
            >Vivamus gravida, nunc egestas faucibus porttitor</span
        >
        <div id="hero-content">
            <div id="hero-text">
                <Title size="large">Igor Moraes</Title>
                <Title size="medium">Front-end & Designer</Title>
                <p>
                    Transformando ideias em realidade através de design e
                    desenvolvimento web. Vem conhecer alguns dos meus projetos!
                </p>
                <img src="../assets/images/raven.svg" alt="Logo de um corvo" />
            </div>
            <div id="hero-buttons">
                <ButtonPrimary :link="link_matrix" style="margin-bottom: 1.5rem"
                    >Entrar em contato</ButtonPrimary
                >
                <ButtonSecondary
                    link="https://www.instagram.com/igor.f.moraes/"
                    :image="Instagram"
                    >Instagram</ButtonSecondary
                >
            </div>
        </div>
    </section>
</template>
<style scoped>
section {
    position: relative;
}
p {
    margin-top: 0.5rem;
    margin-bottom: 1.5rem;
    font: var(--body-medium);
    color: var(--color-text);
    letter-spacing: -0.2px;
}
span {
    margin-bottom: 4rem;
    font-family: "Anchrish Runes";
    font-size: 1.219rem;
    opacity: 30%;
    font-weight: 400;
    display: block;
    text-align: center;
}
img {
    position: absolute;
    width: min(70%, 15rem);
    top: 18%;
    left: 35%;
    z-index: -1;
}

@media (min-width: 1024px) {
    #hero-content {
        display: grid;
        grid-template-columns: 1fr 1fr;
        column-gap: 5.5rem;
        align-items: center;
    }
    span {
        text-align: left;
        margin-bottom: 6.2rem;
    }
    img {
        width: min(30%, 15rem);
        top: 25%;
        left: 18%;
    }
}
</style>
