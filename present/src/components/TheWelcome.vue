<template>
  <div class="shopping">
    <h2>Shopping Cart</h2>
    <div v-if="cart.length === 0">
      <p>No items in the cart</p>
    </div>
    <div v-else>
      <div v-for="(item) in cart" :key="item.name" class="cart-item">
        <h2>{{ item.name }}</h2>
        <h3>{{ item.price }}</h3>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from "vue"; 

const props = defineProps({
  cart: Array,
});
</script>

<style scoped>
.shopping { 
  background-color: black;
  color: white;
  padding: 20px;
  margin-bottom: 10px;
  margin-top: 20%;
}

h2, h3 { 
  background-color: black;
  color: white;
}

.cart-item {
  margin-bottom: 10px;
}
</style>
