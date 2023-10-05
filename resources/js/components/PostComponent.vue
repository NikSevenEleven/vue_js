<script setup>
import SinglePostComponent from "./SinglePostComponent.vue";
let data =
    {
        name: 'Vasia',
        age: 20,
        married: true,
        arr: [3 , 5, 15],
    }
</script>
<template>
    <div><SinglePostComponent></SinglePostComponent></div>
    <div>Name:{{data.name}}</div>
</template>

<style scoped>

</style>
