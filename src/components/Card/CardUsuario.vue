<template>
    <div class="card-usuario">
        <slot name="nome">
            <h3>Nome não encontrado</h3>
        </slot>
        <slot name="link">
            <a href="#">link não encontrado</a>
        </slot>
    </div>
</template>

<style scoped>
.card-usuario {
    border: solid 2px gray;
    padding: 2rem;
    margin: 1rem;
}
</style>
