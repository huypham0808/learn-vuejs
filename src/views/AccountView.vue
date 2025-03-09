<script setup>
import { ref } from 'vue';

  const products = ref([
    {
      id: 1,
      name: "Account 1",
      title: "Software Engineer I"
    },
    {
      id: 2,
      name: "Account 2",
      title: "Software Engineer II"
    },
    {
      id: 3,
      name: "Account 3",
      title: "Software Engineer III"
    },
  ])

</script>


<template>
    <div class="account">
      <h1>This is an My account page</h1>
      <div v-for="product in  products">
          <div class="group-item-product">
            <div>{{ product.id }}</div>
            <div>{{ product.name}}</div>
            <div>{{ product.title }}</div>
          </div>
      </div>
    </div>
</template>
  
  <style>
  @media (min-width: 1024px) {
    .account {
      min-height: 100vh;
      align-items: center;
      color: blue;
    }
    .account .roup-item-product {
      color: yellow;
    }
  }
  </style>
  