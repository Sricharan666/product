<template>
  <div class="container">
    <div >
      <h1 class="page-text">your cart</h1>
      <div class="products">
        <div v-for="(product, index) in cart" :key="index" class="card">
          <img :src="product.image" class="card-img-top"/>
          <div class="card-body">
            <h5 class="card-title">{{ product.Tablet_Name }}</h5>
          <div class="cost card-text">{{ product.Tablet_Price }}</div>
          <button v-on:click="removeItemFromCart(product)" class="btn btn-primary">remove to cart</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
    name : "CartPage",
    props : ["cart"],
    methods :{
        removeItemFromCart(product){
            this.$emit("removeItemFromCart", product)
        }
    }
};
</script>
<style scoped>
</style>