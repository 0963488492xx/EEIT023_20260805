<script setup>
import { computed, useSlots } from "vue";
const props = defineProps({
  size: {
    type: String,
    default: "md"
  },
  text: {
    type: String,
    required: true
  },
  icons: {
    tpye: Array,
    required: true
  }
})

const slots = useSlots()

const isEmpty = computed(() => slots.icon ,slots.default)
</script>

<template>
  <!-- 判斷複層是否有提供 slot 內容-->
   <!-- $slots -->
    <button :class="['btn',' btn-danger',' mb-1', 'btn-color1', `btn-${props.size}`] " >
        <i :class="icons"></i>
        {{ text }}

      
      <slot>預設文字</slot>
        
        </button>
</template>

<style scoped>
.btn-color1 {
  --bs-btn-color: #fff;
  --bs-btn-bg: #7c3aed;
  --bs-btn-border-color: #7c3aed;
  --bs-btn-hover-color: #fff;
  --bs-btn-hover-bg: #6d28d9;
  --bs-btn-hover-border-color: #6d28d9;
  --bs-btn-active-color: #fff;
  --bs-btn-active-bg: #5b21b6;
  --bs-btn-active-border-color: #5b21b6;
  --bs-btn-disabled-color: #fff;
  --bs-btn-disabled-bg: #c4b5fd;
  --bs-btn-disabled-border-color: #c4b5fd;
}
</style>