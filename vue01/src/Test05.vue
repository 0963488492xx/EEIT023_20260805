<script setup>
import { ref } from "vue";

const count = ref(0)
let count2 = 0

const handleClick = () => {
    count.value++
}

const handleClick2 = () => {
    count2++
}

function handleClick3 (num){
    count.value+=num
}
// function handleClick() {
    
// }
</script>

<template>
    <h1>{{ count }}</h1>
    <button v-on:click="handleClick2">點擊</button>
    <button @click="count++">直接增加</button>
    <button @click="handleClick3(3)">傳參數</button>
</template>

<style scoped></style>