<!-- <template>
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
 -->







 <template>
  <h2>Shopping Cart</h2>
  <div class="shopping">
    <div v-if="cart.length === 0">
      <p>No items in the cart</p>
    </div>
    <div v-else>
      <div class="shop-card">
        <div v-for="item in cart" :key="item.name" class="cart-item">
          <h3>{{ item.name }}</h3>
          <img :src="item.img" alt=""/>
          <h4>{{ item.price }}</h4>
          <button @click="removecard(item)" class="gone"> Remove from Cart</button> 
        </div>
      </div>
    </div>
  </div>
  <h3>Total Price: ${{ calculateTotal() }}</h3>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  destination: Object,
  cart: Array
});

function calculateTotal() {
  let total = 0; // Reset total to 0 each time calculateTotal is called
  props.cart.forEach(item => {
    total += item.price;
  });
  return total;
}


function removecard() { 
            const button = document.querySelectorAll(".gone");
            button.forEach((button) => 
            button.addEventListener ("click", function (button){
                button.target.parentElement.remove()}))
              return calculateTotal()};
       



</script>

<style scoped>
.shopping {
  
  color: white;
  padding: 20px;
  margin-bottom: 10px;
  align-items: center;
  height: 50%;
  display: flex;
    flex-wrap: wrap;
    flex-direction: row;
    justify-content: space-around;
    align-content: center;
}



h2 { color: black;
  margin-top: 10%;}

h4, h3, .cart-item, p {
  background-color: black;
  color: white;
  text-align: center;
}

.cart-item { 
  width: 37vw;
}

img {
width: 16vw;
height: 25vh;
}
</style>
