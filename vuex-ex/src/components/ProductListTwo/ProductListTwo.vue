<template>
  <div id="product-list-two">
    <h2>Product list two</h2>
    <ul>
      <li v-for="product in saleProducts">
        <span class="name">{{product.name}}</span>
        <span class="price">{{product.price}}</span>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'app',
    computed: {
      products() {
        return this.$store.state.products;
      },
      saleProducts() {
        return this.$store.getters.saleProducts;
      }
    },
  }
</script>
