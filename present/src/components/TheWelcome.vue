<template>
  <div class="shopping">
    <h2>Shopping Cart</h2>
    <div class="hola" v-if="cart && cart.length === 0">
      <p>No items in the cart</p>
    </div>
    <div v-else>
        <h2>{{ Item.name }}</h2>
        <h3>{{ Item.price }}</h3>


      </div>
    </div>
</template>


<script setup>




const props = defineProps({
  cart: Array,
  Item: Object,
 
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
