<script setup> //phai co setup moi dung dc userRouter method
import { useRouter } from 'vue-router'

const router = useRouter();
</script>
<template>
  <div class="about">
    <button @click="router.push({name: 'aboutUser'})">Navigate to user</button>
    <router-view></router-view>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
