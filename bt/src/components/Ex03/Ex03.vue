<template>
  <div>
    <h1>Ex03</h1>
    <h4>Acreage: {{ width * height }}</h4>
    <button @click="handleChange">Change data</button>
  </div>
</template>

<script setup>
import { ref } from "vue";

const width = ref(10);
const height = 20;
const handleChange = () => {
  width.value += 10;
};
</script>

<style>
</style>