<script setup>
import TechCard from "./TechCard.vue";
</script>
<template>
    <TechCard>
        <template #title>A Estética</template>
        <template #content>
            <img
                width="1.6875rem"
                src="../assets/images/tools/tool-photoshop.svg"
                alt="Logo do Photoshop"
            />
            Photoshop e
            <img
                width="1.6875rem"
                src="../assets/images/tools/tool-figma.svg"
                alt="Logo do Figma"
            />
            Figma são o que uso para fazer as composições, prototipagem e artes
            dos projetos.
        </template>
        <template #buttons>
            <button @click="$emit('change-to', 'front')">anterior</button>
            <button @click="$emit('change-to', 'others')">próximo</button>
        </template>
    </TechCard>
</template>
