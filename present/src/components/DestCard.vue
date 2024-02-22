<template>
    <div class="card">
        <h2>{{ Destination.name }}</h2>
        <img :src="Destination.img" alt=""/>
        <h3>{{ Destination.price }}</h3>
        <button @click="addToCart"> Add to Cart</button> 
    </div>

    <div class="shopping">
    <h2>Shopping Cart</h2>
    <div class = "hello" v-if="cart.length === 0">
      <h2>{{ cart.length }}</h2>
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
import { ref } from 'vue';

const cart = ref([]); 

const props = defineProps({
  Destination: Object,
});

function addToCart() { 
  cart.value.push(props.Destination); // Use props.Destination to access the Destination object
  console.log(cart.value);
}
</script>



<style scoped>
.card {
  width: 32%;
  background-color: rgb(13, 93, 162);
}

h2, h3 {
  background-color: rgb(13, 93, 162);
}

button {
  background-color: rgb(13, 93, 162);
  margin-left: 30%;
}

img {
  width: 70%;
  height: 70%;
  margin-left: 14%;
}
</style>











<!-- 

function totalprice (){ 
    const totprice = 0;
     for ( let i=0; i<cart.length; i++){
        const each = cart [i]
        totprice + each.Destination.price;
        
     }
     return totprice;
    }
    
    function totprice () {
        addto(Destination);
        return total.value;
    } -->


<!--     <div class ="shopping">
        <h2>Shopping Cart</h2> 
        <div v-for="item in cart" :key="item.name">
        <h2>{{ item.name }}</h2>
        <h3>{{ item.price}}</h3>
    </div></div> -->
    
<!--     <div class = "tot">
        <h3> Total Price: ${{ totprice ()}}</h3>
    </div> -->

    