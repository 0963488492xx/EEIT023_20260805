<script setup>
import {ref, reactive} from 'vue'

const fruits = ref([
  { id: 1, name: '蘋果' },
  { id: 2, name: '香蕉' },
  { id: 3, name: '橘子' },
])
const newFruit = ref('');
const profile = reactive({
  姓名: '小明',
  年齡: 25,
  信箱: 'ming@example.com',
  城市: '台北'
});


const addFruit = () => {
    if(newFruit.value == '') return
    const id = Date.now
    const name = newFruit.value
    fruits.value.push({id, name})
    newFruit.value = ''
}
</script>

<template>
    <ul>
        <li v-for="fruit in fruits" :key="fruit.id">
            {{ fruit.name }}
        </li>
    </ul>
    <hr>
    <ul class="ul2">
        <li v-for="(fruit, index) in fruits" :key="fruit.id">
            [{{ index + 1 }}] {{ fruit.name }}
            <button @click="fruits.splice(index, 1)">刪除</button>
        </li>
    </ul>
    <hr>
    <input type="text" v-model.trim="newFruit">
    <button @click="addFruit">新增</button>
    <hr>
    <h3>個人資料</h3>
    <div v-for="(value, key) in profile" :key="key">
        {{ key }} : {{ value }}
    </div>
</template>

<style scoped>
.ul2{
    li{
        display: flex;
        /* flexbox 中的推擠 */
        button{
            margin-left: auto;
        }
    }
}
</style>