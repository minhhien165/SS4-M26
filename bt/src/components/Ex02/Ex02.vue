<template>
  <div>
    <h1>Ex02</h1>
    <p>Company:{{ user.company }}</p>
    <p>Age:{{ user.age }}</p>
    <button @click="handleChangeData">Change data</button>
  </div>
</template>

<script setup>
import { reactive } from "vue";
const newUser = reactive({
  company: "Rikkei academy",
  age: 2,
});
const user = reactive({
  company: "Rikkei education",
  age: 1,
});
const handleChangeData = () => {
  (user.company = newUser.company), (user.age = newUser.age);
};
</script>

<style>
</style>