<template>
  <div>
    <h1>Giới tính: {{ gender }}</h1>
    <div>
        Nam<input  v-model="gender" type="radio"  value="nam"  name="gender">
        Nữ<input   v-model="gender" type="radio"   value="nữ"  name="gender">
        Khác<input v-model="gender"  type="radio" value="khác" name="gender">
    </div>
  </div>
</template>

<script  setup>
import { ref } from 'vue';

const gender=ref('')
</script>

<style>

</style>