<template>
  <el-button
          :disabled="!product.inventory"
          @click="addToCart(product)">
    Add to cart
  </el-button>
</template>

<script>
  import { mapActions } from 'vuex';

  export default {
    props: {
      product: Object,
    },
    methods: mapActions([
      'addToCart',
    ]),
  };
</script>
