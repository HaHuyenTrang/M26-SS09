<template>
  <div>
   <h1> TwowayDatabinding</h1>
   <form @submit.prevent="handleSubmit" action="">
        <h1>UserName: {{ userInfo.userName }}</h1>
        <h1>DateOfBirth: {{ userInfo.dateOfBirth }}</h1>
        <h1>Gender: {{ userInfo.gender }}</h1>
        <h1>Hobbies: {{ userInfo.hobbies }}</h1>
        <h3>Thêm mới người dùng</h3>
        <div>Họ và tên: <input v-model="userInfo.userName" type="text" placeholder="Nhập tên"> </div>
        <div>Ngày sinh: <input v-model="userInfo.dateOfBirth" type="date" placeholder="Nhập ngày sinh"> </div>
        <div>Giới tính:  </div>
        <div>
            Nam <input  value="0" v-model="userInfo.gender" name="gender"  type="radio">
            Nữ <input   value="1" v-model="userInfo.gender" name="gender" type="radio">
            Khác <input value="2" v-model="userInfo.gender" name="gender"  type="radio">
        </div>
        <div>sở thích</div>
        <div>  
            Bóng đá    <input     v-model="userInfo.hobbies" value="socer"  type="checkbox">
            Code         <input   v-model="userInfo.hobbies" value="code" type="checkbox">
            Bơi lội       <input  v-model="userInfo.hobbies" value="swim"  type="checkbox">
            Bóng chuyền   <input  v-model="userInfo.hobbies" value="volleyball"  type="checkbox">
        </div>
        <button>Thêm</button>
   </form>
  </div>
</template>

<script setup>
import { reactive, ref } from 'vue';

// const userName = ref("")
// const dateOfBirth = ref('')
// const gender = ref("")
// const hobbies = ref([])


const userInfo = reactive({
    userName:"",
    dateOfBirth: "",
    gender:"0",
    hobbies:[],
})
const handleSubmit =(e)=>{
    // const user={
    //     userName: userName.value,
    //     dateOfBirth: dateOfBirth.value,
    //     gender: gender.value,
    //     hobbies: hobbies.value
    // };
    console.log("submit", userInfo);

}
</script>

<style>

</style>