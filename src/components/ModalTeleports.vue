<template>
    <div>
        <button @click="toggle">modal</button>
    </div>
    <teleport to='body'>
        <div v-if="show" class="modal">
            <h1>Titulo</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam recusandae natus qui, enim dolorem quasi placeat id! In, soluta quia necessitatibus mollitia provident quam quis, vitae vel harum, veniam inventore.</p>
            <button @click="toggle">cerrar</button>
        </div>
    </Teleport>
</template>
<script setup>
import { ref } from 'vue';

const show = ref(false);

const toggle = () => {
show.value = !show.value;
};
</script>
<style scoped>
.modal {
    position: fixed;
    z-index: 999;
    top: 20%;
    left: 50%;
    width: 300px;
    margin-left: -150px;
    background-color: rgba(0, 0, 0, 0.685);
    color: white;
    padding: 4rem;
}
</style>