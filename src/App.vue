<template>
  <div>
    <header>
      <button @click="navigateTo('products')">View Products</button>
      {{ cart.length }} in cart
      <button @click="navigateTo('cart')">View Cart</button>
    </header>
    <!-- {{page}} -->

    <div v-if="page === 'cart'">
       <CartPage v-on:removeItemFromCart="removeItemtoCart" :cart="cart"/>
    </div>
    <div v-if="page === 'products'">
       <ProductsPage v-on:addd-item="addItemtoCart"/>
    </div>
  
  </div>
</template>

<script>
import ProductsPage from './components/ProductsPage.vue';
import CartPage from './components/CartPage.vue';
export default {
  name: "App",
  data() {
    return {
      page: "products",
      cart: [],
    };
  },
  methods: {
    addItemtoCart(product) {
      this.cart.push(product);
      console.log(this.cart);
    },
    navigateTo(page){
           this.page = page;
    },
    removeItemtoCart(product){
      this.cart.splice(this.cart.indexOf(product) , 1);
    }

  },
  components: {
    ProductsPage,
    CartPage,
  },
};
</script>
<style>
.products {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap :20px;
}
.card{
 /* width : 280px; */
 text-align : center;
 transition: transform 3s ease;
}
.each-item:hover .for-zoom-img{
  overflow: hidden;
}
.each-item:hover .cost{
  display: block;
}
.each-item:hover .card-img-top{
 transform: scale(1.5); 
 transition: transform 1s ease;
}
.cost{
  display: none;
}
.container{
 margin: auto;
}
.page-text{
  text-align: center;
}
img{
  width : 200px;
  height: 200px;
}
.products button {
  padding: 10px;
  background-color: black;
  color: white;
  outline: none;
  border: none;
  cursor: pointer;
}
</style>
<style scoped>

header {
  height: 100px;
  background-color: #eee;
  box-shadow: 2px 2px 5px #999;
  text-align: right;
  font-size: 20px;
  padding-top: 20px;
}
header button {
  padding: 10px;
  border: none;
  cursor: pointer;
  color: white;
  background-color: green;
}
</style>
