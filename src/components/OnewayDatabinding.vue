<template>
    <div>
      <h1>One Way Databinding</h1>
      <h3>UserName : {{ userName }}</h3>
      <input type="text" :value="userName">
      <button @click="handleChangeName">Change Name</button>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  
  const userName = ref("Huyền Trang");
  const handleChangeName = ()=>{
    userName.value = "Hà Huyền Trang"
  }
  </script>
  
  <style></style>