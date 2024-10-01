<template>
  <div>
    <h1>Bai 10</h1>
    <h3>Đăng nhập tài khoản</h3>
    <form @submit.prevent="handleSubmit">
      <label for="email">Email:</label><br />
      <input type="email" id="email" v-model="loginData.email" />
      <br />
      <span v-if="errors.email">{{ errors.email }}</span
      ><br />

      <label for="password">Mật khẩu:</label><br />
      <input type="password" id="pass" v-model="loginData.pass" />
      <br />
      <span v-if="errors.pass">{{ errors.pass }}</span
      ><br /><br />

      <button type="submit">Đăng nhập</button>
    </form>

    <div v-if="loginMessage">{{ loginMessage }}</div>
  </div>
</template>

<script setup>
import { reactive, ref } from "vue";
const loginData = reactive({
  email: "",
  pass: "",
});
const errors = reactive({
  email: "",
  pass: "",
});
const loginMessage = ref("");

const validateForm = () => {
  let valid = true;

  if (!loginData.email) {
    errors.email = "Email không được để trống";
    valid = false;
  } else {
    errors.email = "";
  }

  if (!loginData.pass) {
    errors.pass = "Mật khẩu không được để trống";
    valid = false;
  } else {
    errors.pass = "";
  }

  return valid;
};

const handleSubmit = () => {
  if (validateForm()) {
    const storedData = JSON.parse(localStorage.getItem("user"));

    if (
      storedData &&
      storedData.email === loginData.email &&
      storedData.pass === loginData.pass
    ) {
      alert("Đăng nhập thanh công");
    } else {
      alert("Đăng nhập thất bại");
    }
  }
};
</script>

<style>
span {
  color: red;
}
</style>
