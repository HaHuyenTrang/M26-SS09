<template>
  <div>
    <h1>sở thích: {{ hobbies }}</h1>
    <div>  
            Bóng đá    <input     v-model="hobbies" value="socer"  type="checkbox">
            Code         <input   v-model="hobbies" value="code" type="checkbox">
            Bơi lội       <input  v-model="hobbies" value="swim"  type="checkbox">
            Bóng chuyền   <input  v-model="hobbies" value="volleyball"  type="checkbox">
        </div>
  </div>
</template>

<script  setup>
import { ref } from 'vue';

const hobbies=ref([])
</script>

<style>

</style>