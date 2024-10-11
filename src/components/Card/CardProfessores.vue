<script setup>
import Avatar from "./Avatar.vue";

const props = defineProps({
    nome: String,
    avatar: String,
    linguagem: String,
});
</script>

<template>
    <div class="card">
        <Avatar :urlImg="avatar" />
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

h3 {
    color: #fff;
    font-size: 1.5rem;
}
</style>
