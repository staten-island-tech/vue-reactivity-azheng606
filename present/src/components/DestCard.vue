<template>


    <div class="card" >
        <h2>{{ Destination.name }}</h2>
        <img :src="Destination.img" alt=""/>
        <h3> {{ Destination.price }}</h3>
        <button @click = "increment">Click me</button>
    </div>

    <div class="cart">
        <h3>{{ clicked }}</h3>
    </div>
</template>

<script setup>
import {ref} from "vue";
const props = defineProps ({ 
    Destination: Object,
});

//clicker logic 
const clicked = ref(0);
function increment (){ 
   Destination.price (push)
 clicked.value++;
}
</script>

<style scoped>
.card {
width: 32% ;
background-color: aliceblue;}

img {
    width: 70% ;
}
</style>

