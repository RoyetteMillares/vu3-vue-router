<script setup>
import { useRoute, RouterView } from 'vue-router';
import cars from '../data/cars.json'

const route = useRoute()

const car = cars.find(c => c.id === parseInt(route.params.id))

</script>


<template>
    <section>
        <h1>cars view</h1>
        <p>Name: {{ car.name }}</p>
        <p>Price: {{ car.price }}</p>
        <p>Year: {{ car.year }}</p>
        <RouterView />
    </section>

</template>



<style scoped>

</style>