<script>
import CreateCards from "./CreateCards.vue";
export default {
  data() {
    return {
      cart: [],
    };
  },
  methods: {
    display: function () {
      console.log(this.cart);
    },
    removeItems: function (items) {
      this.cart = this.cart.filter((t) => t !== items);
    },
  },
};
</script>

<template>
  <div>
    <sub>
      <button class="shoppingCartBtn" @click="display()">
        <img
          class="shoppingCartBtn"
          src="https://www.models-resource.com/resources/big_icons/49/48807.png?updated=1666220257"
          alt="Img of Nintedo E shop bag as a shopping cart"
        />
      </button>
    </sub>
    <sub class="cartDisplay" v-for="items in cart" :key="items"
      ><button class="removeItems" @click="removeItems(items)">
        Remove Item</button
      >{{ items.name }} {{ items.price }}</sub
    >
  </div>
</template>

<style>
.shoppingCartBtn {
  width: 20rem;
  height: 20rem;
  margin-right: 10rem;
}

.cartDisplay {
  display: flex;
  flex-direction: row;
  /* --------------------------- */
  font-size: 4rem;
  margin-right: 1rem;
  /*  --------------------------- */
  color: black;
}

.removeItems {
  width: 10rem;
  margin-right: 1rem;
}
</style>
