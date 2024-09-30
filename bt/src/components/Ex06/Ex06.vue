<template>
  <div>
    <h1>Ex06</h1>
    <input type="number" v-model="price" />
    <button @click="addToCart">Add to Cart</button>
    <p>Tổng tiền trong giỏ hàng: {{ totalAmount }}</p>
  </div>
</template>
  
  <script setup>
import { ref, computed } from "vue";

const price = ref(0);

const total = ref(0);

// Thuộc tính computed để tính tổng tiền
const totalAmount = computed(() => total.value);

const addToCart = () => {
  if (price.value > 0) {
    total.value += price.value;
    price.value = 0;
  }
};
</script>
  
  <style>
</style>
  