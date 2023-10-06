<script setup>
import SinglePostComponent from "./SinglePostComponent.vue";
import {ref} from 'vue'
import {reactive} from 'vue'
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
const persons = ref([
    {   id:1,
        name: 'Ivan',
        age: 20,
        job: 'coach',
    },
    {   id:2,
        name: 'Elena',
        age: 25,
        job: 'developer',
    },
    {   id:3,
        name: 'Igor',
        age: 30,
        job: 'coach',
    },
])
const myObject = reactive({
    title: 'How to do lists in Vue',
    author: 'Jane Doe',
    publishedAt: '2016-04-10'
})


</script>
<template>
    <div><SinglePostComponent></SinglePostComponent></div>
    <table class="table">
        <thead>
        <tr>
            <th scope="col">Id</th>
            <th scope="col">Name</th>
            <th scope="col">Age</th>
            <th scope="col">Job</th>
        </tr>
        </thead>
        <tbody>
        <tr v-for="person in persons">
            <th scope="row">{{ person.id }}</th>
            <th scope="row">{{ person.name }}</th>
            <th scope="row">{{ person.age }}</th>
            <th scope="row">{{ person.job }}</th>
        </tr>
        </tbody>
    </table>
    <br>
    <li v-for="(value, key) in myObject">
        {{ key }}: {{ value }}
    </li>

</template>

<style scoped>

</style>
