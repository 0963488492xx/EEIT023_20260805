<script setup>
import { ref } from 'vue'
const message = ref('你好 Vue!')
const name = ref('Ben Chen')
const count = ref(0)
let count2 = 0
const isVisible = ref(true)
<<<<<<< HEAD
const items = ref(['蘋果','香蕉','橘子'])
=======
const items = ref(['蘋果', '香蕉', '橘子'])
>>>>>>> 7b0d7b2706a4c9a343df76a09d722c1eddb30554

count.value++
count2++
items.value.push('草莓')
items.value[count.value] = '香蕉香蕉'
</script>

<template>
  <h1>{{ message }}</h1>
  <h2>{{ name }}</h2>
  <h3>{{ count }}</h3>
  <h3>{{ isVisible }}</h3>
  <h3>{{ items[count] }}</h3>
  <h3>{{ items[count2] }}</h3>
</template>

<style scoped>
h1 {
  color: #42b883;
}
</style>
