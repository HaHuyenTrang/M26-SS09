<template>
  <div>
    <h1>màu sắc <input v-model="qrColor" type="color" placeholder="màu sắc"></h1>
    <h3>mã màu: {{ qrColor }}</h3>
  </div>
</template>

<script  setup>
import { ref } from 'vue';

const qrColor=ref('')
</script>

<style>

</style>