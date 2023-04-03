<script>
export default {
  name: "cart",

  props: {
    name: String,
    price: String,
    cartLength: Number,
  },
  data() {
    return {};
  },
  emits: {},
};
</script>

<template>
  <div id="shoppingCart">
    <sub class="cartDisplay"
      ><span
        ><button class="removeItems">Remove Item</button>Item: {{ name }},
        Price: {{ price }}</span
      ><span></span
    ></sub>
  </div>
</template>

<style>
#shoppingCart {
  display: flex;
  flex-direction: column;
  margin-right: 5rem;
  margin-top: 2rem;
}

.cartDisplay {
  display: flex;
  flex-direction: row;
  /* --------------------------- */
  font-size: 4rem;
  margin-right: 1rem;
  margin-top: 2rem;
  /*  --------------------------- */
  color: aliceblue;
}

.removeItems {
  width: 10rem;
  margin-right: 1rem;
}
</style>
