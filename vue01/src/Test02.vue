<script setup>
import {ref, reactive} from 'vue'

const user = reactive({
    name: "小明",
    age: 25,
    email: "ming@gmail.com"
})
<<<<<<< HEAD
const items = reactive(['蘋果','香蕉','橘子'])
=======
const items = reactive(['蘋果', '香蕉', '橘子'])

>>>>>>> 7b0d7b2706a4c9a343df76a09d722c1eddb30554
user.name = '小美'
user.age = 18
user.email = 'may@gmail.com'
items.unshift('西瓜')
</script>

<template>
<<<<<<< HEAD
    <h1>{{user.name}}</h1>
    <h3>{{user.age}}</h3>
    <h3>{{user.email}}</h3>
    <h3>{{items[0]}}</h3>
=======
    <h1>{{ user.name }}</h1>
    <h3>{{ user.age }}</h3>
    <h3>{{ user.email }}</h3>
    <h3>{{ items[0] }}</h3>
>>>>>>> 7b0d7b2706a4c9a343df76a09d722c1eddb30554
</template>

<style scoped></style>