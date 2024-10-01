<template>
    <div>
      <form @submit.prevent="handleSubmit" action="">
          <h1>Thêm mới tài khoản</h1>
          <h3>Tên sinh viên <input v-model="user.name" type="text" placeholder="nhập tên"></h3>
          <h3>Email <input v-model="user.email" type="email" placeholder="nhập email"></h3>
          <h3>Mật khẩu <input v-model="user.pass" type="password" placeholder="mật khẩu"></h3>
          <h3>Số điện thoại <input v-model="user.phone" type="text"></h3>
          <button @click="handleSubmit">Đăng kí</button>
      </form>
    </div>
  </template>
  
  <script  setup>
  import { reactive, ref } from 'vue';
  
  const user = reactive({
      name:'',
      email:"",
      pass:"",
      phone:""
  })


  const handleSubmit=(e)=>{
      console.log(user);
      if (user.name && user.email && user.pass && user.phone) {
        // Lưu dữ liệu lên localStorage
        localStorage.setItem('user', JSON.stringify(user));

       

        // Xóa hết các giá trị trong ô input
        user.name = '';
        user.email = '';
        user.pass = '';
        user.phone = '';

        // Focus vào ô input Tên sinh viên
        setTimeout(() => {
            document.querySelector('input[type="text"]').focus();
        }, 0);
    } else {
 
    }
  }

  </script>
  
  <style>
  
  </style>