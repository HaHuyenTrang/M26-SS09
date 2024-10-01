<template>
  <div>
    <h1>email <input v-model="newEmail" type="text" placeholder="Nhập email"></h1>
    <h3> giá trị email: {{ newEmail }}</h3>

  </div>
</template>

<script setup>
import { ref } from 'vue';

const newEmail = ref('')
</script>

<style>

</style>