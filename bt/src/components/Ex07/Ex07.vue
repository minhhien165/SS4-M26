<template>
  <div>
    <input type="number" v-model="price" />
    <button @click="addToCart">Add To Cart</button>
    <p>
      Tổng số tiền trong giỏ hàng: {{ total }} và giá trị bình phương:
      {{ square }}
    </p>
  </div>
</template>
  
  <script setup>
import { computed, ref, watch } from "vue";

const price = ref(0);

const total = ref(0);

const addToCart = () => {
  if (price.value > 0) {
    total.value += price.value;
    price.value = 0;
  }
};

// Theo dõi sự thay đổi của total
watch(total, (newValue, oldValue) => {
  console.log(`Giá trị cũ: ${oldValue} và giá trị mới: ${newValue}`);
});

// Thuộc tính computed để tính bình phương của tổng
const square = computed(() => {
  return total.value ** 2;
});
</script>
  
  <style>
</style>
  