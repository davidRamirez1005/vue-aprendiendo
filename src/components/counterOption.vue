<template>
<div>
    <h3>{{ counter }}</h3>
    <button @click="addCounter">Incrementar</button>
</div>
</template>

<script>
import { ref } from 'vue';

export default {
name: 'counterOption',
setup() {
    const counter = ref(0);
    const addCounter = () => {
    counter.value++;
    };

    return {
    counter,
    addCounter
    };
}
};
</script>

<style scoped>
</style>
