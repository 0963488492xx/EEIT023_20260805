<script setup>
import MyButton4 from './components/MyButton4.vue';
</script>

<template>
  <div class="container py-3">
    <MyButton4 text="註冊" size="sm" :icons="['fa-solid', 'fa-right-to-bracket']"/>
    <br>
    <MyButton4 text="登入" :icons="['fa-solid', 'fa-right-to-bracket']"/>
    <br>
    <MyButton4 text="加入我的最愛" size="lg" :icons="['fa-solid', 'fa-star']"/>



  </div>

</template>

<style scoped></style>