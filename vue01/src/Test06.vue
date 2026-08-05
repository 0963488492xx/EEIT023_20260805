<script setup>
const handleSubmit = function(event){
    event.preventDefault()
}

const handleSubmit2 = () => {
    console.log("wwwww");
}

function handleEnter(){
    console.log("按了一下 ENTER");
    
}
</script>

<template>
    <!-- <form action="" @submit="handleSubmit"> -->
    <form action="" @submit.prevent.once="handleSubmit2">
        <label>姓名</label>
        <input type="text" name="name"><br>
        
        <button>送出</button>
    </form>
    <input type="text" @keyup.enter="handleEnter"><br>
</template>

<style scoped></style>