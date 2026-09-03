<script setup>
import { ref } from 'vue'

const key1 = ref('A')
</script>

<template>
    <h1>{{ key1 }}</h1>
    <input type="text" v-model="key1">
    <div v-show="key1 == 'A'">A</div>
    <div v-show="key1 == 'B'">B</div>
<<<<<<< HEAD
    <div v-show="key1 != 'A' && key1 != 'B' ">C</div>
=======
    <div v-show="key1 != 'A' && key1 != 'B'">C</div>
>>>>>>> 7b0d7b2706a4c9a343df76a09d722c1eddb30554
</template>

<style scoped></style>