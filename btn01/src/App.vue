<script setup>
import MyButton1 from './components/MyButton1.vue';
</script>

<template>
  <div class="container py-3">
    <MyButton1 size="sm">
      <template #default>
        註冊
      </template>
      <template #icon>
        <i class="fa-regular fa-address-card"></i>
      </template>
    </MyButton1>

    <br>

    <MyButton1>
            <template #icon>
        <i class="fa-solid fa-right-to-bracket"></i>
      </template>
      登入
    
    </MyButton1>

    <br>

    <MyButton1 size="lg">
      加入我的最愛
      <!-- #icon 原始寫法 v-slot:icon -->
          <template #icon>
        <i class="fa-solid fa-star"></i>
      </template>
    </MyButton1>

  </div>

</template>

<style scoped></style>