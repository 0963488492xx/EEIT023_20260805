<script setup>
<<<<<<< HEAD
import { ref } from "vue";
=======
import {ref} from 'vue'
>>>>>>> 7b0d7b2706a4c9a343df76a09d722c1eddb30554

const count = ref(0)
let count2 = 0

const handleClick = () => {
    count.value++
}

const handleClick2 = () => {
    count2++
}

<<<<<<< HEAD
function handleClick3 (num){
    count.value+=num
}
// function handleClick() {
    
// }
=======
function handleClick3(num){
    count.value+=num
}
>>>>>>> 7b0d7b2706a4c9a343df76a09d722c1eddb30554
</script>

<template>
    <h1>{{ count }}</h1>
<<<<<<< HEAD
    <button v-on:click="handleClick2">點擊</button>
=======
    <button v-on:click="handleClick">點擊</button>
>>>>>>> 7b0d7b2706a4c9a343df76a09d722c1eddb30554
    <button @click="count++">直接增加</button>
    <button @click="handleClick3(3)">傳參數</button>
</template>

<style scoped></style>