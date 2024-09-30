<template>
    <div>
        <h1>Ex08</h1>
      <h2>Giỏ hàng</h2>
      <ul>
        <li v-for="item in products" :key="item.id">
          {{ item.name }}: {{ item.quantity }}
          <button @click="increaseQuantity(item.id)">Tăng số lượng</button>
        </li>
      </ul>
      <div>Tổng số lượng sản phẩm: {{ totalQuantity }}</div>
    </div>
  </template>
  
  <script setup>
  import { computed, reactive } from 'vue';
  
  const products = reactive([
    {
      id: 1,
      name: "loại 1",
      quantity: 5,
    },
    {
      id: 2,
      name: "loại 2",
      quantity: 3,
    },
    {
      id: 3,
      name: "loại 3",
      quantity: 2,
    },
  ]);
  
  const totalQuantity = computed(() => {
    return products.reduce((acc, item) => acc + item.quantity, 0);
  });
  
  const increaseQuantity = (id) => {
    const product = products.find(item => item.id === id);
    if (product) {
      product.quantity += 1;
    }
  };
  </script>
  
  <style>
  h2 {
    margin-bottom: 10px;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    margin: 5px 0;
  }
  button {
    margin-left: 10px;
  }
  </style>
  