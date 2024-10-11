<script setup>
import Titulo from "./components/Titulo.vue";
import CardProfessores from "./components/CardProfessores.vue";

const professores = [
    {
        id: 1,
        nome: "Elton",
        avatar: "https://github.com/elton-fonseca.png",
        linguagem: "PHP",
    },
    {
        id: 2,
        nome: "Amauri",
        avatar: "https://www.github.com/AmauriBlanco.png",
        linguagem: "JavaScript",
    },
    {
        id: 3,
        nome: "Cleyson",
        avatar: "https://github.com/CleysonPH.png",
        linguagem: "Python",
    },
];
</script>

<template>
    <Titulo texto="Professores" />

    <div class="card-container">
        <CardProfessores
            v-for="professor in professores"
            :key="professor.id"
            :nome="professor.nome"
            :avatar="professor.avatar"
            :linguagem="professor.linguagem"
        />
    </div>
</template>

<style scoped>
.card-container {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
}
</style>
