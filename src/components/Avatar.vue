<script setup>
const props = defineProps({
    urlImg: String,
});
</script>

<template>
    <img :src="urlImg" :alt="none" width="140px" />
</template>

<style scoped>
img {
    border-radius: 50%;
    border: solid 3px green;
}
</style>
