<script setup>
import { ref, defineEmits } from "vue";

const texto = ref("");
const emit = defineEmits(["enviar"]);

function enviarMensagem() {
    emit("enviar", texto.value);
}
</script>

<template>
    <input type="text" v-model="texto" />
    <button @click="enviarMensagem">Enviar</button>
</template>
