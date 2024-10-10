<script setup>
const props = defineProps({
    nome: String,
    avatar: String,
    linguagem: String,
});
</script>

<template>
    <div class="card">
        <img :src="avatar" :alt="none" width="150px" />
        <h3>{{ nome }}</h3>
        <p>Linguagem: {{ linguagem }}</p>
    </div>
</template>

<style scoped>
.card {
    background-color: #2b2b2b;
    padding: 1.5rem;
    border-radius: 10px;
    max-width: 200px;
    text-align: center;
}

img {
    border-radius: 50%;
    border: solid 3px green;
}

h3 {
    color: #fff;
    font-size: 1.5rem;
}
</style>
