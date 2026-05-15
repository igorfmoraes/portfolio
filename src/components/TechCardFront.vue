<script setup>
import TechCard from "./TechCard.vue";
</script>
<template>
    <TechCard>
        <template #title>A Essência</template>
        <template #content>
            <img
                width="1.6875rem"
                src="../assets/images/tools/tool-nuxt.svg"
                alt="Logo do Nuxt"
            />
            Nuxt e
            <img
                width="1.6875rem"
                src="../assets/images/tools/tool-vue.svg"
                alt="Logo do Vue"
            />
            Vue são bibliotecas para construir interfaces web excepcionais e dar
            vida aos sites.
        </template>
        <template #buttons>
            <button aria-hidden="true" tabindex="-1" disabled class="inactive">
                anterior
            </button>
            <button @click="$emit('change-to', 'design')">próximo</button>
        </template>
    </TechCard>
</template>
