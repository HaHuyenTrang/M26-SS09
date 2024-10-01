<template>
  <div>
    <h1>tiến độ hoàn thành : {{ inputRange }} %</h1>
    <input v-model="inputRange" type="range">
  </div>
</template>

<script setup>
import { ref } from 'vue';

const inputRange=ref('')
</script>

<style>

</style>