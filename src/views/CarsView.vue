<script setup>
import { useRoute } from 'vue-router';
import cars from '../data/cars.json'

const route = useRoute()

const car = cars.find(c => c.id === parseInt(route.params.id))

</script>


<template>
    <section>
        <h1>cars view</h1>
        <p>{{ car }}</p>
    </section>

</template>



<style scoped>

</style>