<template>
   <div>
      <Card v-for="item in shoppingData" :key="item.id" :item="item" /> 
   </div>
</template>

<script>
import Card from '@/components/Card.vue';

export default {
   name: 'Home',
   props: [
      'shoppingData',
   ],
   components: {
      Card,
   },
}
</script>

<style scoped>
div {
   display: flex;
   flex-direction: row;
   flex-wrap: wrap;
   justify-content: space-evenly;
   gap: 15px;
   align-items: stretch;   
}
</style>