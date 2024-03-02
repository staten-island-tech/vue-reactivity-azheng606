<template>
  <div class="card">
    <h2>{{ destination.name }}</h2>
    <img :src="destination.img" alt=""/>
    <h3>{{ "$" + destination.price }}</h3>
    <button @click="addToCart"> Add to Cart</button>
  </div>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue';
const props = defineProps({
 destination: Object,
 cart: Array
});
const emits = defineEmits(['addtocart']);
function addToCart () {
 emits('addtocart', props.destination);
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
margin-left: 40%;
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