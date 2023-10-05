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

function sayJob()
{
    return this.data.name +' работает в булочной'
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
    <div>Job:{{sayJob()}}</div>
    <div><button @click="sayHello">Hello</button></div>
    <div><button @click="sayHi">Hi</button></div>

</template>

<style scoped>

</style>
