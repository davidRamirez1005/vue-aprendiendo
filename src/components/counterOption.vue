<template>
<div>
    <h3>{{ counter }}</h3>
    <button @click="addCounter">Incrementar</button>
</div>
</template>

<script setup>
import { ref } from 'vue';

const counter = ref(0);
const addCounter = () => {
counter.value++;
};
</script>

<style scoped>
</style>
