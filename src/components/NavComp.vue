<script setup>
import {RouterLink} from 'vue-router';
</script>

<template>
    <div>
        <p><RouterLink active-class="active" to="/">Home</RouterLink></p>
        <p><RouterLink  active-class="active" to="/about">About</RouterLink></p>
    </div>

    
</template>


<style  scoped>

.active{
    font-weight: 900;
    color: rgb(187, 233, 114)yellow;
    font-size: 30px;
}

</style>