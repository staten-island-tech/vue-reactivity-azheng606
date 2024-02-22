<template>
  <div class="shopping">
    <h2>Shopping Cart</h2>
    <div class = "hello" v-if="cart.length === 0">
      <h2>{{ cart.length }}</h2>
      <p>No items in the cart</p> 
    </div>
    <div v-else>
      <div v-for="(item, index) in cart" :key="index">
        <h2>{{ item.name }}</h2>
        <h3>{{ item.price }}</h3>

      </div>
    </div>
  </div>
</template>

<script setup>


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

.hello { background-color: black;}

p { background-color: black;}
.cart-item {
  margin-bottom: 10px;
}
</style>
