
<template>

<div>
    <div class="card" >
        <h2>{{ Destination.name }}</h2>
        <img :src="Destination.img" alt=""/>
        <h3> {{ Destination.price }}</h3>
    
        <button @click = "addto(Destination)">Add to Cart</button>
    </div>

    <div class ="shopping">
        <h2>Shopping Cart</h2> 
        <div v-for="item in cart" :key="item.name">
        <h2>{{ item.name }}</h2>
        <h3>{{ item.price}}</h3>
    </div></div>
    
    <div class = "tot">
        <h3> Total Price: ${{ totprice ()}}</h3>
    </div>
</div>

</template>



<script setup>
import {ref} from "vue";
const props = defineProps({
  Destination: Object,
});


//clicker logic 
const total = ref(0);
const cart = ref([]);

function addto (Destination) {
     cart.value.push (Destination);
    total.value = totalprice(); 
}

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
}
</script>

<style scoped>
.card {
width: 32% ;
background-color: aliceblue;
}

img {
    width: 70% ;
    height: 70%;
}

</style>

