<script setup>
import cars from '../data/cars.json'
import { RouterLink } from 'vue-router';

</script>

<template>
  <main>
    <h1>Home page</h1>

    <div class="cars-wp">
      <RouterLink v-for="car in cars" :key="car.id" :to="`/cars/${car.id}`">
        {{ car.name }}
      </RouterLink>
    </div>

  </main>
</template>


<style scoped>
.cars-wp {
  display: flex;
  gap: 2rem;
}

a {
  text-decoration: none;
  padding: 0.75rem;
  color: #000;
  width: 100%;
  box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.8);
}
</style>