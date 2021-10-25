<template>
  <div class="product">
    <div class="product-image">
      <img v-bind:src="image" />
    </div>
    <div class="product-info">
      <h1>{{ product }}</h1>
      <p v-if="inventory > 10">In Stock</p>
      <p v-else-if="inventory <= 10 && inventory > 0">Almost Sold Out!</p>
      <p v-else>Out of Stock</p>
    </div>
  </div>
</template>

<script>
import greenSock from "../assets/vmSocks-green.jpg";

export default {
  name: "Products",
  props: {},

  data() {
    return {
      product: "Socks",
      image: greenSock,
      inventory: 11,
    };
  },
};
</script>

<style scoped>
.product {
  display: flex;
  flex-flow: wrap;
  padding: 1rem;
}

img {
  border: 1px solid #d8d8d8;
  width: 70%;
  margin: 40px;
  box-shadow: 0px 0.5px 1px #d8d8d8;
}

.product-image {
  width: 80%;
}

.product-image,
.product-info {
  margin-top: 10px;
  width: 50%;
}
</style>
