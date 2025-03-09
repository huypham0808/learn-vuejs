<script setup> //phai co setup moi dung dc userRouter method
  import { ref } from 'vue';
  import ChildComponent from '../components/ChildComponent.vue'


  const testCount = ref(10);
</script>
<template>
  <div>Hello</div>
    <!-- <button @click="router.push({name: 'aboutUser'})">Navigate to user</button>
    <router-view></router-view> -->
    <ChildComponent :testCountView="testCount"/>
</template>

<style>
</style>
