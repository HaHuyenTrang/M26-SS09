<template>
  <div>
    <form @submit.prevent="handleSubmit" action="">
        <h1>Thêm mới tài khoản</h1>
        <h3>Họ và tên <input v-model="user.name" type="text" placeholder="nhập tên"></h3>
        <h3>Email <input v-model="user.email" type="email" placeholder="nhập email"></h3>
        <h3>Mật khẩu <input v-model="user.pass" type="password" placeholder="mật khẩu"></h3>
        <button>Đăng kí</button>
    </form>
  </div>
</template>

<script  setup>
import { reactive } from 'vue';

const user = reactive({
    name:'',
    email:"",
    pass:"",
})
const handleSubmit=(e)=>{
    console.log(user);
    
}
</script>

<style>

</style>