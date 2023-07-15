<template>
    <div>
        <form action="">
            <!-- v-model => permite crear enlaces bidireccionales entre un elemento de entrada de datos (como un <input>, <textarea>, o <select>) y una propiedad en la instancia de Vue. -->
            <input type="text" v-model="inputText" >
        </form>
        <h3>{{inputText}}</h3>
    </div>
    <div>
        <select v-model="opcion">
        <option value="opcion1">Opción 1</option>
        <option value="opcion2">Opción 2</option>
        <option value="opcion3">Opción 3</option>
    </select>
    <p>La opción seleccionada es: {{ opcion }}</p>
    </div>
</template>
<script setup>
import { ref } from 'vue'

    let inputText = ref('')
    let opcion = ref('')
</script>
<style scope>

</style>