<script setup>
import MyButton3 from './components/MyButton3.vue';
</script>

<template>
  <div class="container py-3">
    <MyButton3 size="sm">
      <template #default>
        註冊
      </template>
      
    </MyButton3>

    <br>

    <MyButton3>
            <template #icon="{iconClass}">
        <i :class="['fa-solid', 'fa-right-to-bracket', iconClass]"></i>
      </template>
      登入
    
    </MyButton3>

    <br>

    <MyButton3 size="lg">
      加入我的最愛
      <!-- #icon 原始寫法 v-slot:icon -->
          <template #icon="{iconClass}">
        <i :class="['fa-solid', 'fa-star', iconClass]"></i>
      </template>
    </MyButton3>

  </div>

</template>

<style scoped></style>