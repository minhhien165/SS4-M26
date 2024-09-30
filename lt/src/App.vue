<template>
  <div>
    <h1>Ref, Reactive, computed, watcher</h1>

    <h2>Ref</h2>
    <p>gia tri bien count : {{ count }}</p>
    <button @click="increase">click</button>
    <p>Reactive</p>
    <p>******************</p>
    <p>computed</p>
    <p>gia tri cua bien count {{ numberCount }}</p>
    <p>gia tri bien count khi binh phuong {{ calculator }}</p>
    <button @click="handleClickk">Click</button>

    <ul>
      <li>name: {{ userInfor.name }}</li>
      <li>address: {{ userInfor.address }}</li>
    </ul>
    <button @click="changeInfo">Change info</button>
    <p>************************</p>
    <p>Watcher</p>
    <button @click="handleIncrease">increase</button>
  </div>
</template>

<script setup>
import { ref, reactive, computed, watch } from "vue";
const count = ref(0); // {value:0}
const numberCount = ref(5);
const number = ref(1);
const userInfor = {
  id: 1,
  name: "Ngoc Nguyen",
  address: "Thanh Oai",
};
const increase = () => {
  count.value++;
};
const user = reactive({
  fullName: "Nguyen Thach Kim Ngoc",
  age: 19,
  address: "Ha Noi",
});
const changeInfo = () => {
  userInfor.value.address = "Tran Phu";
  userInfor.value.name = "Ai Nhi";
};
const calculator = computed(() => {
  return numberCount.value ** 2;
});
const handleClickk = () => {
  numberCount.value *= 2;
};
watch(number, (newValue, oldValue) => {
  // thuong di xu ly call API
  console.log("watch dc goi!");
  console.log("gia tri OldValue", oldValue);
  console.log("gia tri NewValue", newValue);
});
const handleIncrease = () => {
  number.value++;
};
</script>

<style>
</style>