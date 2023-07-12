<template>
    <div>
        <!--
        ? selectiva con if-else 
        * solo indica el nodo que se esta usando y el otro lo ignora,  deja un nodo mas pequeño, mas limpio
        -->
        <h1 v-if="age > 18">eres mayor de edad</h1>
        <h1 v-else>eres menor de edad</h1>

                <!--
        ? selectiva con show
        * indica que nodo se esta usando y que no en el html con una clase display none, es agil para cuando se va ejecutar pocas veces
        -->
        <h1 v-show="nombre=='jose'">hola jose david</h1>
        <h1 v-show="nombre=='david'">hola jajaj</h1>
    </div>
</template>

<script setup>
    let age = 20
    let nombre = "jose"
</script>
<style scope>
H1{
    color: blue;
}
</style>