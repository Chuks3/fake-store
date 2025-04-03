<template>
  <div class="product-card">
    <router-link to="/product-details/" class="inner-container">
      <img :src="item.image" class="card-image">
      <p class="card-text">{{ item.title }}</p>
      <p class="card-price">${{ item.price }}</p>
    </router-link>
  </div>
</template>

<script>
import router from '@/router';

export default {
  name: 'Card',
  props: {
    item: {},
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.product-card {
  display: flex;
  flex-direction: column;
  flex-basis: 30%;
  max-width: 300px;
  box-shadow: 5px 5px 15px 5px rgba(0, 0, 0, 0.35);
  margin-bottom: 25px;
	font-family: "Montserrat", sans-serif;
  background: #fff;
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
  height: 260px;
  width: 260px;
}
.product-card .card-price {
  position: absolute;
  bottom: 10px;
  left: 0;
  right: 0;
}
</style>
