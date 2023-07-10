<template>
  <button @click="show = !show">Menu</button>
  <transition name="fade">
    <ul v-show="show">
      <li>opcion 1</li>
      <li>opcion 2</li>
      <li>opcion 3</li>
    </ul>
  </transition>
</template>

<script>
export default {
  name: 'MenuBarra',
  data() {
    return {
      show: false
    };
  }
};
</script>

<style scoped>
.fade-leave-active,
.fade-enter-active {
  transition: opacity 0.5s ease;
}
.fade-leave-to {
  opacity: 0;
}
.fade-enter-from {
  opacity: 0;
}

ul {
  list-style: none;
  display: flex;
  justify-content: center;
  padding: 0;
  margin: 0;
}

li {
  margin: 0 10px;
  cursor: pointer;
}

li:hover {
  text-decoration: underline;
}
</style>
