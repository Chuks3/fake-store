<template>
   <main>
      <h1>Product Details Page</h1>
      <div class="product-card">
         <img :src="data.image" class="card-image">
         <h2 class="card-text">{{ data.title }}</h2>
         <h2 class="card-price">${{ data.price }}</h2>
      </div>
      <button>Add to Cart</button>
   </main>
</template>

<script>
export default {
   name: 'ProductDetails',
   props: ['id'],
   data() {
    return {
      data: [],
    }
  },

  created: function () {
    this.getShoppingData()
  },

  methods: {
    getShoppingData() {
      fetch('https://fakestoreapi.com/products/' + this.id)
            .then(res=>res.json())
            .then(json=> this.data = json)
    }
  }

}
</script>

<style scoped>
main {
   background-color: #fff;
   height: 92vh;
}
h1 {
   color: #0a0a0a;
   padding: 10px 0px;
   text-transform: uppercase;
}
.product-card {
  display: flex;
  flex-direction: column;
  flex-basis: 30%;
  max-width: 400px;
  /* box-shadow: 5px 5px 15px 5px rgba(0, 0, 0, 0.35); */
  /* margin-bottom: 25px; */
  margin: 0 auto;
  font-family: "Montserrat", sans-serif;
  /* background: #fff; */
  border-radius: 5px;
}
.product-card a {
  color: #0a0a0a;
  text-decoration: #0a0a0a;
}
.product-card .inner-container{
  padding: 20px;
  position: relative;
  padding-bottom: 50px;
  height: 100%;
}
.product-card .card-image {
  height: 400px;
  width: 400px;
}
button {
   width: 20%;
   height: 43px;
   font-size: 20px;
   border-radius: 5px;
   background-color: #0a0a0a;
   color: #fff;
   font-weight: bold;
   cursor: pointer;
   padding: 10px 0;
}
</style>