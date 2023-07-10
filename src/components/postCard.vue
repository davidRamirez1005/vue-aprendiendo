<template>
    <div class="post-card">
        <h3>titulo </h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. At ab accusamus animi provident similique ipsum non consequuntur, est neque autem odio ex quidem libero ipsam eius omnis sed maiores voluptatum?</p>
        <postBtn />
    </div>
</template>
<script setup>
    import postBtn from './postBtn.vue'

</script>
<style scoped>
.post-card{
    padding: 1rem;
    margin: 1rem;
    border-radius: 1rem;
    border: 1px solid #ccc;
}
</style>