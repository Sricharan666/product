<template>
  <div class="container">
    <h1 class="page-text">Products</h1>
    <div class="products">
      <div v-for="(product, index) in products" :key="index" class="card">
        <div class="each-item">
          <div class="each-div">
            <div class="for-zoom-img">
              <img :src="product.image" class="card-img-top" />
            </div>
            <div class="card-body">
              <h5 class="card-title">{{ product.Tablet_Name }}</h5>
              <div class="cost card-text">
                <p>{{ product.Description }}</p>
              </div>
              <div>
                <h6>{{ product.Tablet_Price }}</h6>
              </div>
              <!-- <button v-on:click="addItemtoCart(product)">Add to cart</button> -->
              <button v-on:click="addItem(product)" class="btn btn-primary">
                Add to cart
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "ProductsPage",
  data() {
    return {
      showDescription: false,
      products: [
        {
          Tablet_Name: "cetirizine tablets",
          Tablet_Price: "$0.99",
          image:
            "https://4.imimg.com/data4/MU/BW/MY-4092588/cetirizine-tablets-500x500.jpg",
          Description:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus fugit consequuntur",
        },
        {
          Tablet_Name: "paracetamol tablets",
          Tablet_Price: "$2.34",
          image:
            "https://media.istockphoto.com/id/157402355/photo/generic-paracetamol-isolated-on-white.jpg?s=612x612&w=0&k=20&c=2E3oCvsuOhbB8jmDmDgIFrPDg_FLyEvp-K0IdvGagaw=",
          Description:
            "nobis ex! Quae provident fugiat neque aliquam, nesciunt consequatur, ex cupiditate recusandae, amet esse ea excepturi ducimus qui itaque",
        },
        {
          Tablet_Name: "Pantoprazole tablets",
          Tablet_Price: "$2.34",
          image:
            "https://5.imimg.com/data5/SELLER/Default/2021/5/BQ/MH/DT/87360600/pantoprazole-40-mg-tablets-500x500.jpg",
          Description:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus fugit consequuntur",
        },
        {
          Tablet_Name: "solvin cough tablets",
          Tablet_Price: "$2.34",
          image:
            "https://newassets.apollo247.com/pub/media/catalog/product/s/o/sol0240_2_feb23.jpg",
          Description:
            "nobis ex! Quae provident fugiat neque aliquam, nesciunt consequatur, ex cupiditate recusandae, amet esse ea excepturi ducimus qui itaque",
        },
        {
          Tablet_Name: "Nutrition vitamin-D tablets",
          Tablet_Price: "$2.34",
          image: "https://m.media-amazon.com/images/I/71RVHEJk-cL._SL1500_.jpg",
          Description:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus fugit consequuntur",
        },
        {
          Tablet_Name: "Eucee vitamin-C tablets",
          Tablet_Price: "$2.34",
          image:
            "https://elybrate.in/wp-content/uploads/2021/05/Buy-eucee-vitamin-c-Vitamin-C-Chewing-500-mg.jpg",
          Description:
            "nobis ex! Quae provident fugiat neque aliquam, nesciunt consequatur, ex cupiditate recusandae, amet esse ea excepturi ducimus qui itaque",
        },
        {
          Tablet_Name: "vitamin-B complex tablets",
          Tablet_Price: "$2.34",
          image: "https://m.media-amazon.com/images/I/51e5RcaotxL._SL500_.jpg",
          Description:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus fugit consequuntur",
        },
        {
          Tablet_Name: "Fizovit tablets",
          Tablet_Price: "$2.34",
          image: "https://m.media-amazon.com/images/I/8117K+vMQmL._SL1500_.jpg",
          Description:
            "nobis ex! Quae provident fugiat neque aliquam, nesciunt consequatur, ex cupiditate recusandae, amet esse ea excepturi ducimus qui itaque",
        },
        {
          Tablet_Name: "Evion tablets",
          Tablet_Price: "$2.34",
          image: "https://m.media-amazon.com/images/I/61cx7rywsuL._SL1280_.jpg",
          Description:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus fugit consequuntur",
        },
        {
          Tablet_Name: "Calcitrex tablets",
          Tablet_Price: "$2.34",
          image: "https://m.media-amazon.com/images/I/51GzLJMVbfL.jpg",
          Description:
            "nobis ex! Quae provident fugiat neque aliquam, nesciunt consequatur, ex cupiditate recusandae, amet esse ea excepturi ducimus qui itaque",
        },
        {
          Tablet_Name: "Vitamin b12 tablets",
          Tablet_Price: "$2.34",
          image:
            "https://www.netmeds.com/images/product-v1/600x600/815779/healthvit_vitamin_b12_methylcobalmin_1000mcg_tablets_60_s_0.jpg",
          Description:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus fugit consequuntur",
        },
        {
          Tablet_Name: "Calcium vitamin-D3 tablets",
          Tablet_Price: "$2.34",
          image: "https://m.media-amazon.com/images/I/61r0lkx3JmS._SY450_.jpg",
          Description:
            "nobis ex! Quae provident fugiat neque aliquam, nesciunt consequatur, ex cupiditate recusandae, amet esse ea excepturi ducimus qui itaque",
        },
        {
          Tablet_Name: "Calfer tablets",
          Tablet_Price: "$2.34",
          image:
            "https://4.imimg.com/data4/VR/OJ/MY-2163542/cap-calfer-500x500.jpg",
          Description:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus fugit consequuntur",
        },
        {
          Tablet_Name: "Tramodol tablets",
          Tablet_Price: "$2.34",
          image:
            "https://tapentadolmed.com/wp-content/uploads/2021/08/tttra-300x300.jpg",
          Description:
            "nobis ex! Quae provident fugiat neque aliquam, nesciunt consequatur, ex cupiditate recusandae, amet esse ea excepturi ducimus qui itaque",
        },
        {
          Tablet_Name: "Dermet tablets",
          Tablet_Price: "$2.34",
          image: "https://drbest.in/wp-content/uploads/2019/06/DrMet-GB.jpg",
          Description:
            "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Delectus fugit consequuntur",
        },
        {
          Tablet_Name: "Purecure tablets",
          Tablet_Price: "$2.34",
          image:
            "https://rukminim1.flixcart.com/image/312/312/kdkkdjk0/ayurvedic/t/t/u/60-glow-blood-purifying-formula-for-healthy-skin-tablet-pure-original-imafufnxgt7gbzaj.jpeg?q=70",
          Description:
            "nobis ex! Quae provident fugiat neque aliquam, nesciunt consequatur, ex cupiditate recusandae, amet esse ea excepturi ducimus qui itaque",
        },
      ],
    };
  },
  methods: {
    addItem(product) {
      this.$emit("addd-item", product);
      console.log("here", product);
    },
    showDetails() {
      this.showDescription = true;
    },
    hideDetails() {
      this.showDescription = false;
    },
  },
};
</script>
<style scoped>
</style>
