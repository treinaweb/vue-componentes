<script setup>
import Titulo from "./components/Global/Titulo.vue";
import CardProfessores from "./components/Card/CardProfessores.vue";
import CardUsuario from "./components/Card/CardUsuario.vue";
import FormularioInput from "./components/Global/FormularioInput.vue";
import BlocoTexto from "./components/Global/BlocoTexto.vue";

import { provide, ref } from "vue";

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

const mensagem = ref("");

function enviarMensagem(novaMensagem) {
    mensagem.value = novaMensagem;
}

const texto = "Essa mensagem está vindo do App.vue";
provide("textoCompartilhado", texto)
</script>

<template>
    <main>
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
        <Titulo texto="Conhecendo os slots" />
        <CardUsuario>
            <template #nome>
                <h3>Amauri</h3>
            </template>
            <template #link>
                <a href="#">Meu link</a>
            </template>
        </CardUsuario>

        <CardUsuario>
            <template #nome>
                <h3>Segundo Nome</h3>
            </template>
            <template #link>
                <a href="#">tenho link</a>
            </template>
        </CardUsuario>
        <div>
            <Titulo texto="Conhecendo os Emits" />
            <FormularioInput @enviar="enviarMensagem" />
            <p>Valor digitado foi: {{ mensagem }}</p>
        </div>

        <div>
            <Titulo texto="Conhecendo Providers e Inject" />
            <BlocoTexto/>
        </div>
    </main>
</template>

<style scoped>
.card-container {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
}

main {
    margin-bottom: 500px;
}

h1 {
    margin-top: 13rem;
}
</style>
