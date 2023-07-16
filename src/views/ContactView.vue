<script setup>
import { useRoute } from 'vue-router';

import cars from '../data/cars.json'

const routes = useRoute()

const car = cars.find(car=> car.id === parseInt(routes.params.id));
console.log(car);
</script>


<template>
    <div>
        <h1>Contact Info</h1>
        <p>{{car.contact.dealer}}</p>
        <p>{{car.contact.number}}</p>
    </div>
</template>