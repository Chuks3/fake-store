<template>
  <main>
    <NavBar/>
    <router-view :shoppingData="shoppingData"/>
  </main>
</template>

<script>
import NavBar from './components/NavBar.vue'

export default {
  name: 'App',
  components: {
    NavBar, 
  },

  data() {
    return {
      shoppingData: [],
    }
  },

  created: function () {
    this.getShoppingData()
  },

  methods: {
    getShoppingData() {
      fetch('https://fakestoreapi.com/products')
            .then(res=>res.json())
            .then(json=> this.shoppingData = json)
    }
  }
}
</script>

<style>
@import url("https://fonts//googleapis.com/css2?family=Montserrat:wght@100;400;800$display=swap");
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body {
	background: #282c34;
}
</style>
