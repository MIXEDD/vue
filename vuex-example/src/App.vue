<template>
  <div id="app">
    <product-list-one v-bind:products="products"></product-list-one>
    <product-list-two v-bind:products="products"></product-list-two>
  </div>
</template>

<script>

  import ProductListOne from './components/ProductListOne/ProductListOne.vue';
  import ProductListTwo from './components/ProductListTwo/ProductListTwo.vue';

export default {
  name: 'app',
  data () {
    return {
      products: [
        {name: 'Banana Skin',price:20},
        {name: 'Shiny Start',price:40},
        {name: 'Green Shells',price:60},
        {name: 'Red Shells',price:80}
      ]
    }
  },
  components: {
    'product-list-one': ProductListOne,
    'product-list-two': ProductListTwo
  }
}
</script>
