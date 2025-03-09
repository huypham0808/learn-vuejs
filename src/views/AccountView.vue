<script setup>
import { ref } from 'vue';

  const categoryProduct = ref('food')
  const products = ref([
    {
      id: 1,
      name: "Pizza",
      category: "Food"
    },
    {
      id: 2,
      name: "Tra sua",
      category: "Drink"
    },
    {
      id: 3,
      name: "Com Chien",
      category: "Food"
    },
    {
      id: 4,
      name: "Nuoc mia",
      category: "Drink"
    },
  ])
const handleCategoryProduct = (value) => {
  categoryProduct.value = value;
} 
</script>


<template>
    <div class="account">
      <h1>This is an My List page</h1>
      <button @click="handleCategoryProduct('food')">Show Food</button>
      <button @click="handleCategoryProduct('drink')">Show Drink</button>
      <!-- <div v-for="product in  products">
          <div class="group-item-product">
            <div>{{ product.id }}</div>
            <div>{{ product.name}}</div>
            <div>{{ product.title }}</div>
          </div>
      </div> -->
      <div v-if="categoryProduct === 'food'">Hien thi Danh sach Food</div>
      <div v-else>Hien thi Danh sach Drink</div>
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
  