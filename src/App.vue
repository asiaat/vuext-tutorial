<template>
  <div id="app">
   <product-list-one></product-list-one>
   <product-list-two></product-list-two>
    
    
  </div>
</template>

<script>

import ProducListOne from './components/ProductListOne.vue'
import ProducListTwo from './components/ProductListTwo.vue'

export default {


  components: {
      'product-list-one': ProducListOne,
      'product-list-two': ProducListTwo,
  }, 

  name: 'app',
  data () {
    return {
      
    }
  }
}
</script>

<style>
#app {
  font-family: Ubuntu;
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
  margin: 0 12px;
}

a {
  color: #42b983;
}
</style>
