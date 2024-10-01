<template>
  <div>
    <form @submit.prevent="handleSubmit" action="">
      <h1>Thêm mới sản phẩm</h1>
      <h3>
        Mã sản phẩm
        <input v-model="product.id" type="text" placeholder="mã sản phẩm" />
      </h3>
      <h3>
        Tên sản phẩm
        <input
          v-model="product.productName"
          type="text"
          placeholder="tên sản phẩm"
        />
      </h3>
      <h3>
        Giá <input v-model="product.price" type="number" placeholder="giá" />
      </h3>
      <h3>số lượng <input v-model="product.quantity" type="number" /></h3>
      <button >Thêm mới</button>
    </form>
  </div>
</template>

<script setup>
import { reactive } from "vue";

const product = reactive({
  id: "",
  productName: "",
  price: "",
  quantity: "",
});
const handleSubmit = (e) => {
    console.log(product);
    
};
</script>

<style></style>
