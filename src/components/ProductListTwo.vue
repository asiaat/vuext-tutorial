<template>
  <div id="product-list-two">
  <h2>Product List Two</h2>    
    <ul>
        <li v-for="product in saleProducts">
           <span class="name"> {{ product.name }}</span>     
           <span class="name"> £{{ product.price }}</span>
        </li>
    </ul>
    <button v-on:click="reducePrice(0.5)">Reduce Price</button>
  </div>
</template>

<script>
import {mapActions} from 'vuex';
import {mapGetters} from 'vuex';

export default {
  computed :{
      products() {
          return this.$store.state.products;
      },
  
     ...mapGetters([
         'saleProducts',
     ])
  },
  methods:{
      ...mapActions([
          'reducePrice'
      ])
  }
    
   
}
</script>