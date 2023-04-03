<template>
  <h2 class="itemCounter"># of items in Cart: {{ cart.length }}</h2>
  <button class="shoppingCartBtn">
    <img
      class="shoppingCartBtn"
      src="https://www.models-resource.com/resources/big_icons/49/48807.png?updated=1666220257"
      alt="Img of Nintedo E shop bag as a shopping cart"
    />
  </button>
</template>

<script>
export default {
  name: "cartButton",
  props: {
    cart: Number,
  },
  data() {
    return {};
  },
};
</script>

<style scoped>
.itemCounter {
  font-size: 4rem;
  color: aliceblue;
}
.shoppingCartBtn {
  width: 15rem;
  height: 15rem;
  margin-right: 10rem;
}
</style>
