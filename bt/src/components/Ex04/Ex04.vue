<template>
  <div>
    <h1>Ex04</h1>
    <input type="text" v-model="inputValue" />
  </div>
</template>
  
  <script setup>
import { ref, watch } from "vue";

const inputValue = ref("");

watch(inputValue, (newVal, oldVal) => {
  console.log(`Giá trị cũ: ${oldVal} và giá trị mới: ${newVal}`);
});
</script>
<style>
</style>
  