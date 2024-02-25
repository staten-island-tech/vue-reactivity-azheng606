<template>
  <div class="card">
    <h2>{{ destination.name }}</h2>
    <img :src="destination.img" alt=""/>
    <h3>{{ destination.price }}</h3>
    <button @click="addToCart"> Add to Cart</button>
  </div>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  destination: Object,
  cart: Array
});

const emits = defineEmits(['add-to-cart']);

function addToCart () {
  emits('add-to-cart', props.destination);
};
</script>

<style scoped>
.card {
  height: 50%;
    width: 25%;
    background-color:#b0a592; ;
    align-items: center;
    border-radius: 5%;
    box-shadow: 10px 5px 5px rgb(70, 72, 73);
    margin: 15px 1px;
}


h2, h3 {
background-color: var(--light);
text-align: center;
}

button {
background-color: var(--secondary);
margin-left: 35%;
}

img {
width: 20vw;
height: 25vh;
margin-left: 9%;
}

:root 
{ 
  --black: #000000;
    --light: #b0a592;
    --dark: #5e3f0b;
    --white: #ffffff;
  --primary: var(--light);
  --secondary:var(--dark);
}
</style>

























<!-- <template>
  <div class="card">
      <h2>{{ Destination.name }}</h2>
      <img :src="Destination.img" alt=""/>
      <h3>{{ Destination.price }}</h3>
     
      <button @click="addToCart"> Add to Cart</button>
  </div>

</template>


<script setup>






const props = defineProps({
Destination: Object,
cart: Array,
Item: Object,
});


function addToCart() {
    props.cart.push(props.Destination);
    console.log(props.cart);
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
.first, .second{
  background-color: black;
  color: white;
}
button {
background-color: rgb(13, 93, 162);
margin-left: 30%;
}
.shopping {background-color: black;
  color: white;}
img {
width: 70%;
height: 70%;
margin-left: 14%;
}
</style>
 -->











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

    