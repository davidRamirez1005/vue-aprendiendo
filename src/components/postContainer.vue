<template>
    <div class="post-container">
        <postCard />
        <postCard />
        <postCard />
        <postCard />
    </div>
</template>
<script setup>
    import PostCard from './postCard.vue';
</script>
<style scoped>
.post-container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100vh;
    flex-wrap: wrap;
}
</style>