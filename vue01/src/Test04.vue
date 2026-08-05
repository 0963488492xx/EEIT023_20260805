<script setup>
import {ref} from 'vue'

const imageUrl = 'https://images.pexels.com/photos/16197273/pexels-photo-16197273.jpeg'
const link = 'https://doc.sagedaben.com/article/eNFWSpbv?theme=class'
const className = "circle"
const isLoading = ref(true)
const textColor = "pink"

</script>

<template>
    <a v-bind:href="link">vue 第一章</a>
    <div :class="className"></div>
    <button :disabled="isLoading">送出</button>
    <!-- 動態切換樣式，像是按 like 愛心的樣式切換就會用到 -->
    <button class="btn" :class="{disable: isLoading}">我是按鈕</button>
    <img :src="imageUrl" alt="">
</template>

<style scoped>
img{
    width: 100%;
}
.circle{
    width: 200px;
    height: 200px;
    border-radius: 50%;
    background-color: #f07979;
}
.btn{
  padding: 4px;
  padding-left: 8px;
  padding-right: 8px;
  width: fit-content;
  background-color: #01aaff;
  border-radius: 5px;
  color: #fff;
  user-select: none;
  cursor: pointer;
  &:hover{
    background-color: #006eff;
  }
  &.disable{
    background-color: #646464;
    cursor: not-allowed;
  }
}

</style>