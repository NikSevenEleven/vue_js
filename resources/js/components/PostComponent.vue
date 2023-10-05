<script setup>
import SinglePostComponent from "./SinglePostComponent.vue";
function sayHello()
{
    alert('Hello')
}

function sayHi()
{
    alert('Hi')
}

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
    <div><button @click="sayHello">Hello</button></div>
    <div><button @click="sayHi">Hi</button></div>
</template>

<style scoped>

</style>
