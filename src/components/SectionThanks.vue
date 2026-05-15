<script setup>
import ButtonPrimary from "./ButtonPrimary.vue";
import Title from "./Title.vue";

const link_matrix =
    "https://matrix.to/#/@igorfmoraes:matrix.org?client=im.fluffychat";
</script>
<template>
    <section id="thanks">
        <Title size="medium">Obrigado por ler até aqui!</Title>
        <Title size="small">Bora criar algo fascinante juntos</Title>
        <ButtonPrimary :link="link_matrix">Entrar em contato</ButtonPrimary>
    </section>
</template>
<style scoped>
#thanks h2,
#thanks h3 {
    text-align: center;
}
#thanks h3 {
    margin-bottom: 1rem;
}
</style>
