<script setup>
const props = defineProps(["image", "link"]);

function open_link() {
    window.open(props.link, "_blank");
}
</script>
<template>
    <div role="button" @click="open_link">
        <img
            v-if="image"
            :src="image"
            :alt="'Logo do ' + $slots.default()[0].children"
            width="1.35rem"
        />
        <a :href="link" target="_blank">
            <slot></slot>
        </a>
    </div>
</template>
<style scoped>
a {
    color: var(--color-white);
    font: var(--body-large);
    line-height: 100%;
    letter-spacing: -0.2px;
    transition: 0.2s;
}
div {
    background-color: var(--color-background);
    border: 2px solid var(--color-white);

    height: 3.5rem;
    border-radius: 0.5rem;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: 0.2s;
}
div:hover {
    background-color: var(--color-white);
    cursor: pointer;
}
div:hover > a {
    color: var(--color-background);
}
img {
    margin-right: 4px;
    width: 1.35rem;
    aspect-ratio: 1 / 1;
    transition: 0.2s;
}
div:hover > img {
    filter: brightness(0) saturate(100%) invert(11%) sepia(6%) saturate(2818%)
        hue-rotate(135deg) brightness(91%) contrast(92%);
}
</style>
