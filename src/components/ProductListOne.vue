<template>
  <div id="product-list-one">
  <h2>Product List One</h2>    
    <ul>
        <li v-for="product in saleProducts">
           <span class="name"> {{ product.name }}</span>     
           <span class="name"> £{{ product.price }}</span>
        </li>
    </ul>
  </div>
</template>

<script>
export default {

  computed :{
      products() {
          return this.$store.state.products;
      },
      saleProducts(){
          return this.$store.getters.saleProducts;
      }
  }
}
</script>

<style scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}


</style>