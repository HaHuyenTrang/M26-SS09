<template>
  <div>
    <h1>Ngày sinh: {{ dateofbirth }}</h1>
    <input v-model="dateofbirth"  type="date">
  </div>
</template>

<script  setup>
import { ref } from 'vue';

const dateofbirth=ref('')
</script>

<style>

</style>