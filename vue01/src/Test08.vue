<script setup>
import { ref } from 'vue'

const key1 = ref('A')
</script>

<template>
    <h1>{{ key1 }}</h1>
    <input type="text" v-model="key1">
    <div v-if="key1 == 'A'">A</div>
<<<<<<< HEAD
    <!-- <div>123<div/> v-if 系列的元素中間被插入沒有 v-if 的會出錯-->
=======
    <!-- <div>123</div> v-if 系列的元素中間被插入沒有 v-if 的會出錯 -->
>>>>>>> 7b0d7b2706a4c9a343df76a09d722c1eddb30554
    <div v-else-if="key1 == 'B'">B</div>
    <div v-else>C</div>
</template>

<style scoped></style>