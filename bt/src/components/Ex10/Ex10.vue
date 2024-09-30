<template>
    <div>
        <h1>Ex10</h1>
      <button @click="showContent">Hiển thị</button>
      <button @click="hideContent">Ẩn</button>
      <h4 v-if="isVisible">Nội dung được hiển thị</h4>
      <h4 v-else>Nội dung bị ẩn</h4>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  // Biến để kiểm soát hiển thị nội dung
  const isVisible = ref(false);
  
  // Hàm để hiển thị nội dung
  const showContent = () => {
    isVisible.value = true;
  };
  
  // Hàm để ẩn nội dung
  const hideContent = () => {
    isVisible.value = false;
  };
  </script>
  
  <style>
  </style>
  