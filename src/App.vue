<template>
  <div id="app">
    <div class="cart">
      <p>Cart({{ cart.length }})</p>
    </div>
    <products :premium="true" @add-to-cart="updateCart" />
  </div>
</template>

<script>
import Products from "./components/Products.vue";

export default {
  name: "App",
  components: {
    Products,
  },

  data() {
    return {
      premium: true,
      cart: [],
    };
  },
  methods: {
    updateCart(id) {
      this.cart.push(id);
    },
  },
};
</script>

<style>
#app {
  font-family: tahoma;
  color: #282828;
  margin: 0px;
}

.cart {
  margin-right: 25px;
  float: right;
  border: 1px solid #d8d8d8;
  padding: 5px 20px;
}
</style>
