<script setup>
import { ref, reactive } from 'vue'

const cardAry = reactive([
    {
        img: 'https://images.pexels.com/photos/13543169/pexels-photo-13543169.jpeg',
        title: '轉讓交友特別是市場價，你們的出版，狀況。',
        content: '正常看見裡面發出推薦使用語音很少簡體如今原本旁邊犯罪五年工資，裝修無派對付丈夫，斗內一人，時代一身。'
    },
  {
    img: "https://images.pexels.com/photos/531844/pexels-photo-531844.jpeg",
    title: "計算機並不一切及時有很多小",
    content: "售價爭取現代批評簡單種子網易持續適應，答應是個趕緊美國禁止控制據說地上具備傳統我一晶片，資料庫，這。"
  },
  {
    img: "https://images.pexels.com/photos/461198/pexels-photo-461198.jpeg",
    title: "常見你們德國要去員工，進入頭髮友情",
    content: "計算機，智能事業機械所需，上班加上消費者，保持願意目前初音資料庫存在區別，這一點小學不多桌面快捷主義不好各個不去，你也註冊三大新臺幣分別只是，協調加強裝備多麼由於，世紀跟我說。"
  },
  {
    img: "https://images.pexels.com/photos/38547/office-freelancer-computer-business-38547.jpeg",
    title: "進攻二手，電視劇，螢",
    content: "自動所需天下尷尬沒人司機貿易分為下載文檔那天訪問女朋友，負責超市希望醫藥也不，德國吃螺。"
  },
  {
    img: "https://images.pexels.com/photos/533325/pexels-photo-533325.jpeg",
    title: "內心重視願意，吃螺絲，現代",
    content: "體驗花園，查找色彩交給，配置必須本月職責之類可愛圍繞，深刻站在從此提高光臨臺中比例書記機構意思，都市馬上國外情節，湖北明顯公共發表遺憾，目光影片一句話唱。"
  }
])

const counter = ref(4)

const nextOne = () => {
    counter.value++
    if(counter.value >= cardAry.length){
        counter.value = 0
    }
}

const prevOne = () => {
    counter.value--
    if(counter.value < 0){
        counter.value = cardAry.length - 1
    }
}
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
                    <div class="btn btn-primary" @click="prevOne">上一個</div>
                    <div class="btn btn-primary" @click="nextOne">下一個</div>
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