<script setup>
//  ref es una función que se utiliza para crear una referencia reactiva en Vue, lo cual significa que cualquier cambio en el valor de la referencia será detectado automáticamente y actualizará las partes relevantes de la interfaz de usuario.
import { ref } from 'vue'
// const show = ref(true): Aquí se crea una referencia reactiva llamada show y se inicializa con el valor booleano true. Esto significa que show es una referencia que puede cambiar y que está asociada a un valor booleano
const show = ref(true)
</script>

<template>
	<button @click="show = !show">Toggle</button>
  <Transition
    name="custom-classes"
    enter-active-class="animate__animated animate__tada"
    leave-active-class="animate__animated animate__bounceOutRight"
  >
    <p v-if="show">hello</p>
  </Transition>
</template>

<style>
@import "https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css";
</style>