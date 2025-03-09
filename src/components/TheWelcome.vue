<script setup>
import { reactive, ref } from 'vue';

  const hello = 'Vuejs 2025';

  const objectType = {
    name: 'Huy Pham',
    title: 'Software Engineer',
  }

  //ref su dung 1 doi tuong va 1 thuoc tinh
  //truy cap thuoc tinh ref bang cach .value

  const count = ref(0);
  const count1 = ref(0);
  //count.value = count.value + 1;
  // reactive cho phep su dung 1 object trong do co nhieu doi tuong, ko nen su dung array trong reactive
  const objectType2 = reactive({
    name: "Huy Dev",
    age: "18"
  });
  // Event trong Vuejs
  const inCreaseEvent = () => {
    count.value = count.value + 1;
  }

  const submitForm = () => {
    count1.value++;
  }
  //Two way binding in Vuejs
  const text = ref('');
</script>

<template>
  <div class="red">My first project using {{ hello }}</div>
  <div>Su dung ref</div>
  <div class="red">Name: {{ objectType.name }}</div>
  <div class="red">Title: {{ objectType.title}}</div>
  <div>Add value {{ count }}</div>
  <div>Su dung reactive</div>
  <div class="orange">Hien thi reactive {{ objectType2.name }}</div>
  <button v-on:click="inCreaseEvent">Increase</button>
  <button @click="inCreaseEvent">Increase2</button>
  <form @submit.prevent="submitForm">
    <div>Add value 1: {{ count1 }}</div>
    <button type="submit">Submit formm</button>
  </form>
  <div>Text with two way binding: {{ text }}</div>
  <input type="text" v-model.trim="text">
</template>
<style>
  .red {
    color: red;
  }
  .orange {
    color: orange;
  }
</style>