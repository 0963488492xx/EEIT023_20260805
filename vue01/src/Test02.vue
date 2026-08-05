<script setup>
import {ref, reactive} from 'vue'

const user = reactive({
    name: "小明",
    age: 25,
    email: "ming@gmail.com"
})
const items = reactive(['蘋果', '香蕉', '橘子'])

user.name = '小美'
user.age = 18
user.email = 'may@gmail.com'
items.unshift('西瓜')
</script>

<template>
    <h1>{{ user.name }}</h1>
    <h3>{{ user.age }}</h3>
    <h3>{{ user.email }}</h3>
    <h3>{{ items[0] }}</h3>
</template>

<style scoped></style>