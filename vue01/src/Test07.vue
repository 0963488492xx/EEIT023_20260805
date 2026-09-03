<script setup>
import { ref } from 'vue'

const userID = ref('123')
const userPassword = ref('')
const userEmail = ref('')

const handleSubmit = ()=>{
    console.log(userID.value, userPassword.value, userEmail.value);
    
}
</script>

<template>
  <form @submit.prevent="handleSubmit">
    <div class="row">
      <label>id</label>
      <input type="text" v-model="userID">
    </div>
    <div class="row">
      <label>password</label>
      <input type="password" v-model="userPassword">
    </div>
<<<<<<< HEAD
     <div class="row">
      <label>email</label>
      <input type="email" v-model="userEmail">
    </div>
    <div class="ctrl">
      <button>送出</button>
    </div>
       
    
=======

    <div class="row">
      <label>email</label>
      <input type="email" v-model="userEmail">
    </div>

    <div class="ctrl">
      <button>送出</button>
    </div>
>>>>>>> 7b0d7b2706a4c9a343df76a09d722c1eddb30554
  </form>
</template>


<style scoped>
.row{
    display: flex;
    input{
        flex: 1;
    }
}
/* .row input{} */

.ctrl{
    display: flex;
    justify-content: flex-end;
}
</style>