<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <MenuBarra v-show="show" />
    <postContainer />
    <counterOption />
    <transitionIr />
    <br><br>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import postContainer from "./components/postContainer.vue";
import MenuBarra from "./components/MenuBarra.vue";
import counterOption from "./components/counterOption.vue";
import transitionIr from './components/transitionIr.vue';

const show = ref(false);
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
