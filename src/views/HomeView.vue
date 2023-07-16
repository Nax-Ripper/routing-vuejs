<script setup>

import cars from '../data/cars.json'

import { RouterLink } from 'vue-router';



</script>


<template>
    <div>
        <h1>Home View</h1>
        <div class="cars">
            <RouterLink :to="`/cars/${car.id}`" href="" v-for="car in cars" :key="car.id">{{car.name}}</RouterLink>
        </div>
    </div>
</template>


<style scoped>
.cars{
    display: flex;
}

.cars a{
    text-decoration: none;
    color: black;
    width: 100%;
    box-shadow: 2px 2px 20px rgba(0,0,0,0.388);
    margin: 15px;
    text-align: center;
    border-radius: 16px;
    padding: 30px 0;
    cursor: pointer;
}

a:hover{
    background-color:greenyellow;
}
</style>