<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <MenuBarra v-show="show" />
    <postContainer />
    <counterOption />
    <transitionIr />
    <br><br>
    <ModalTeleports />
    <br><br>
    <exampleSelective />
    <exampleFor />
    <hasError />
    <br>
    <ModelForm />
    <cicleOption />

  </div>
</template>

<script setup>
import postContainer from "./components/postContainer.vue";
import MenuBarra from "./components/MenuBarra.vue";
import counterOption from "./components/counterOption.vue";
import transitionIr from './components/transitionIr.vue';
import ModalTeleports from './components/ModalTeleports.vue';
import exampleSelective from './components/exampleSelective.vue';
import exampleFor from './components/exampleFor.vue';
import hasError from './components/classBind.vue';
import ModelForm from './components/ModelForm.vue';
import cicleOption from "./components/cicleOption.vue";



</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}

</style>
