<template>
    <div>
        <h1>Ex09</h1>
      <h2>Danh sách Bài Viết</h2>
      <ul>
        <li v-for="product in products" :key="product.id">
          <ul>
            <li>ID: {{ product.id }}</li>
            <li>Tiêu đề: {{ product.title }}</li>
            <li>Nội dung: {{ product.content }}</li>
            <li>Tác giả: {{ product.author }}</li>
          </ul>
        </li>
      </ul>
    </div>
  </template>
  
  <script setup>
  const products = [
    {
      id: 1,
      title: "Bài viết 1",
      content: "Nội dung bài viết 1",
      author: "Tác giả 1"
    },
    {
      id: 2,
      title: "Bài viết 2",
      content: "Nội dung bài viết 2",
      author: "Tác giả 2"
    },
    {
      id: 3,
      title: "Bài viết 3",
      content: "Nội dung bài viết 3",
      author: "Tác giả 3"
    }
  ];
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
    margin: 10px 0;
  }
  </style>
  