<script setup>
import TechCard from "./TechCard.vue";
</script>
<template>
    <TechCard>
        <template #title>E Muitas Outras</template>
        <template #content>
            Tenho contato com diversas ferramentas populares no mercado, sejam
            para edição ou programação.
        </template>
        <template #buttons>
            <button @click="$emit('change-to', 'design')">anterior</button>
            <button aria-hidden="true" tabindex="-1" disabled class="inactive">
                próximo
            </button>
        </template>
    </TechCard>
</template>
