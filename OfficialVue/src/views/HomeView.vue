<script>
import CssVariables from "./CssVariables.vue";
import cart from "./ShoppingCart.vue";
import create from "../components/CreateCards.vue";
export default {
  components: { CssVariables, cart, create },
  data() {
    return {};
  },
  methods: {},
};
</script>

<template>
  <div id="parent">
    <create />
    <cart />
  </div>
</template>

<style scoped></style>
