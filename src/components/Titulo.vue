<script setup>
const props = defineProps({
    texto: String,
});
</script>

<template>
    <h1>{{ texto }}</h1>
</template>

<style scoped>
h1 {
    color: green;
    font-weight: bolder;
    font-size: 3rem;
}
</style>
