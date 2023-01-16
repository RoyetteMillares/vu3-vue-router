<script setup>
import { useRoute, useRouter, RouterView } from 'vue-router';
import cars from '../data/cars.json'

const route = useRoute()
const router = useRouter();

const currentId = parseInt(route.params.id)

const car = cars.find(c => c.id === currentId)

</script>


<template>
    <section>
        <h1>cars view</h1>
        <p>Name: {{ car.name }}</p>
        <p>Price: {{ car.price }}</p>
        <p>Year: {{ car.year }}</p>
        <button @click="router.push(`/cars/${currentId}/contact`)">Contact Us</button>
        <RouterView />
    </section>

</template>



<style scoped>

</style>