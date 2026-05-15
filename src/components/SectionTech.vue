<script setup>
import { shallowRef } from "vue";
import Title from "./Title.vue";
import TechCardFront from "./TechCardFront.vue";
import TechCardDesign from "./TechCardDesign.vue";
import TechCardOthers from "./TechCardOthers.vue";

const card_list = {
    front: TechCardFront,
    design: TechCardDesign,
    others: TechCardOthers,
};
const current_card = shallowRef(TechCardFront);
function change_card(card) {
    current_card.value = card_list[card];
}
</script>
<template>
    <section id="tech">
        <div>
            <Title size="medium">Ferramentas e Tecnologias</Title>
            <p>
                Python e React já são de praxe, vem conhecer as minhas favoritas
                de verdade!
            </p>
            <img
                class="float"
                id="ps"
                src="../assets/images/tools/floating-photoshop.svg"
                alt="Logo do Photoshop"
            />
            <img
                class="float"
                id="vue"
                src="../assets/images/tools/floating-vue.svg"
                alt="Logo do Vue"
            />
        </div>
        <component :is="current_card" @change-to="change_card"></component>
    </section>
</template>
<style scoped>
section {
    position: relative;
}
p {
    font: var(--body-medium);
    letter-spacing: -0.2px;
    margin: 1rem 0;
}
.float {
    width: 4.25rem;
    position: absolute;
}
#ps {
    top: 38%;
    left: -4%;
    transform: rotate(-10.646deg);
    filter: blur(2px);
    z-index: -1;
}
#vue {
    top: 90%;
    right: 0;
    transform: rotate(15deg);
    filter: blur(1px) drop-shadow(-2px 4px 12px #17252633);
}
@media (min-width: 1024px) {
    section {
        display: grid;
        grid-template-columns: 1fr 1fr;
        column-gap: 5.5rem;
    }
    #ps,
    #vue {
        filter: none;
        width: 6rem;
        top: 55%;
        left: 0;
    }
    #vue {
        left: 20%;
    }
}
</style>
