<template>
    <div>
      <h1>Ex01</h1>
      <p v-show="isShow">Rikkei academy</p>
      <button @click="handleShow">Hien</button>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const isShow = ref(true);
  
  const handleShow = () => {
    console.log(isShow.value);
    isShow.value = !isShow.value; 
  };
  </script>
  
  <style>
  </style>
  