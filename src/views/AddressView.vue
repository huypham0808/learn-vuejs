<script setup>
import { ref } from 'vue';
import ChildComponent from '../components/ChildComponent.vue'

const count = ref(3);

const handleIncrease = (value) => {
  count.value = count.value + value;
}

const handleData = (data) => {
  count.value = count.value + data.value;
}
</script>

<template>
    <div class="address">
      <h1>This is an about ADDRESS page</h1>
     <!-- <ChildComponent :testCountView="count" @handle-increase="handleIncrease"/> -->
     <ChildComponent :testCountView="count" @handle-data="handleData"/>
    </div>
  </template>
  
  <style>
  @media (min-width: 1024px) {
    .address {
      min-height: 100vh;
      /* display: flex; */
      align-items: center;
      color: violet;
    }
  }
  </style>
  