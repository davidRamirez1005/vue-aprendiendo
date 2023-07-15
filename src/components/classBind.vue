<template>
    <div>
    <p v-bind:class="{'danger': hasError}">El mensaje se ha enviado satisfactoriamente</p>
    <br>
    <p v-bind:style="{backgroundColor: 'orange', color: color}">El mensaje dos se ha enviado correctamente</p>
    <br>
    <button @click="click">Cambiar color</button>
</div>
</template>

<script setup>
import { ref } from 'vue'

let hasError = ref(true)
let color = ref('#ffaa')
const click = () => {
    color.value = '#ff0000'
}
</script>

<style scoped>
.danger {
    color: red;
}
</style>
