<script setup>
import Titulo from "./components/Titulo.vue";
import CardProfessores from "./components/CardProfessores.vue";
</script>

<template>
    <Titulo texto="Professores" />

    <div class="card-container">
        <CardProfessores
            nome="Elton"
            avatar="https://github.com/elton-fonseca.png"
            linguagem="PHP"
        />
        <CardProfessores
            nome="Amauri"
            avatar="https://www.github.com/AmauriBlanco.png"
            linguagem="JavaScript"
        />
        <CardProfessores
            nome="Cleyson"
            avatar="https://github.com/CleysonPH.png"
            linguagem="Python"
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
