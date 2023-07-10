<script setup>
import { ref } from 'vue'

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