<template>
  <div id="app">
    <products />
  </div>
</template>

<script>
import Products from "./components/Products.vue";

export default {
  name: "App",
  components: {
    Products,
  },
};
</script>

<style>
#app {
  font-family: tahoma;
  color: #282828;
  margin: 0px;
}
</style>
