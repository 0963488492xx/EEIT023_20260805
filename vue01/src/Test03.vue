<script setup>
import {ref, reactive} from 'vue'
const message = 'Hello, Vue!'
const isActive = true
</script>

<template>
    <!-- {{  }} 只能使用在元素當中， 不能使用在元素的屬性裡 -->
    <!-- <img src="" alt=""> src, alt 就是元素的屬性 -->
    <p>訊息: {{ message }}</p>
    <p>計算: {{ 1+1 }}</p>
    <p>呼叫方法: {{message.toUpperCase()}}</p>
    <p>三元運算子: {{ isActive ? '啟用' : '停用' }}</p>
</template>

<style scoped></style>