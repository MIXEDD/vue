<template>
  <div id="app">
    <product-list-one></product-list-one>
    <product-list-two></product-list-two>
  </div>
</template>

<script>

  import ProductListOne from './components/ProductListOne/ProductListOne.vue';
  import ProductListTwo from './components/ProductListTwo/ProductListTwo.vue';

  export default {
    name: 'app',
    data () {
      return {

      }
    },
    components: {
      'product-list-one': ProductListOne,
      'product-list-two': ProductListTwo
    }
  }
</script>
