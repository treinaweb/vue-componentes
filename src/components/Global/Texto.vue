<script setup>
import { inject } from "vue";

const texto = inject("textoCompartilhado");
</script>

<template>
    <div>
        <p>{{ texto }}</p>
    </div>
</template>
