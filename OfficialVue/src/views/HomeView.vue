<script>
import CssVariables from "./CssVariables.vue";
import CreateCards from "./CreateCards.vue";
import ShoppingCart from "./ShoppingCart.vue";
export default {
  components: { CssVariables, ShoppingCart, CreateCards },
  data() {
    return {};
  },
  methods: {},
};
</script>

<template>
  <div id="parent">
    <ShoppingCart />
    <CreateCards />
  </div>
</template>

<style scoped></style>
