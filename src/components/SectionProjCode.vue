<script setup>
import Title from "./Title.vue";
import ProjCard from "./ProjCard.vue";
import EducaSim from "../assets/images/projects/educasim.avif";
import EducaSimDetails from "../assets/images/projects/educasim-details.pdf";
import Cocktail from "../assets/images/projects/cocktail-app.avif";
import Solarium from "../assets/images/projects/solarium.avif";
</script>
<template>
    <section id="projects-code">
        <Title size="medium">Projetos de Desenvolvimento</Title>
        <div class="projects-area">
            <div class="projects-cards">
                <ProjCard
                    :image="EducaSim"
                    :repository="EducaSimDetails"
                    :link="EducaSimDetails"
                >
                    Software educacional em Python focado no ensino de ciências
                    por meio de experimentação ativa e investigativa
                </ProjCard>
                <ProjCard
                    :image="Cocktail"
                    repository="https://github.com/IgorFerreiraMoraes/cocktail-app"
                    link="https://www.instagram.com/reel/CpzqLDBAK0U/"
                >
                    App de pedidos de coquetéis com Vue usando componentes, uma
                    API externa e armazenamento de dados
                </ProjCard>
            </div>
        </div>
    </section>
</template>
<style scoped>
.projects-area {
    margin-top: 1rem;
    min-height: 558px;
    position: relative;
}
.projects-area::before {
    content: "";
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 100vw; /* Make it 100% of the viewport width */
    height: 100%; /* Make it 100% of the .section height */
    background: url("../assets/images/projects/projects-background-code.avif");
    background-size: cover;
    z-index: -1;
}
.projects-cards {
    padding-top: 4rem;
    display: grid;
    grid-template-columns: repeat(2, max(87.39%, 18rem));
    column-gap: 2rem;
    overflow-x: scroll;
}

@media (min-width: 1024px) {
    .projects-area {
        min-height: 762px;
    }
    .projects-area::before {
        background-position: 0 -8rem;
    }
    .projects-cards {
        padding-top: 3rem;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        column-gap: 5.5rem;
        overflow-x: scroll;
    }
}
</style>
