<script setup>
import { ref, reactive } from 'vue'

const cardAry = reactive([
    {
        img: 'https://images.pexels.com/photos/13543169/pexels-photo-13543169.jpeg',
        title: '轉讓交友特別是市場價，你們的出版，狀況。',
        content: '正常看見裡面發出推薦使用語音很少簡體如今原本旁邊犯罪五年工資，裝修無派對付丈夫，斗內一人，時代一身。'
    }
])

const counter = ref(0)
</script>

<template>
    <div class="container py-3">
        <div class="d-flex justify-content-center">
            <div class="card w400px mh300px">
                <img :src="cardAry[counter].img">
                <div class="card-body">
                    <h3 class="fw-bold">{{ cardAry[counter].title }}</h3>
                    <p>
                        {{ cardAry[counter].content }}
                    </p>
                </div>
                <div class="card-footer border-top-0 bg-white d-flex justify-content-between">
                    <div class="btn btn-primary">上一個</div>
                    <div class="btn btn-primary">下一個</div>
                </div>
            </div>
        </div>

    </div>

</template>

<style scoped>
.w400px{
    width: 400px;
}
.mh300px{
    min-height: 300px;
}
</style>