<template>
    <div>
        <ul>
            <li v-for="(pais) in paises" :key="pais">{{pais}}</li>
        </ul>
    </div>
    <br>
    <div>
        <ul>
            <h3  v-for="(animal) in animales" :key="animal">{{ animal }}</h3>
        </ul>
    </div>
    <br>
    <div>
        <ul>
            <h3  v-for="(country) in countries" :key="country.abrev">{{ country.name }} y {{country.animales}}</h3>
        </ul>
    </div>
</template>

<script setup>
import {ref} from 'vue'
let paises = ref([
    'spaña','colombia','argentina','francia'
])
let animales = ref({
    'perro': 'kal',
    'gato': 'luna',
    'pez': 'pescado'
})
let countries = ref([
    {
        'abrev': "es",
        'name': 'Spain',
        'animales': "toro"
    },
    {
        'abrev': 'col',
        'name': 'Colombia',
        'animales': "perro"
    },
    {
        'abrev': 'ar',
        'name': 'Argentina',
        'animales': "pajaro"
    }
])
</script>
<style scope>

</style>