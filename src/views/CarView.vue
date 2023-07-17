
<script setup>
import {useRoute, RouterView, useRouter} from 'vue-router'
import cars from '../data/cars.json';
import ContactView from './ContactView.vue'

const route = useRoute();
const router = useRouter();
console.log(route);
console.log(router)
// userRoute is to extract info
// userRouter is to do operation with router
const car =cars.find(car=> car.id === parseInt(route.params.id))
</script>

<template>
    <div v-if="car">
        <h1>Car View</h1>
        <p>{{car.name}}</p>
        <p>{{car.year}}</p>
        <p>{{car.price}}</p>
        <button @click="router.push(`/cars/${car.id}/contact`)">Click for contact</button>
        <p><RouterView></RouterView></p>
    </div>
    <div v-else>
        <h1>Car not found</h1>
    </div>
</template>