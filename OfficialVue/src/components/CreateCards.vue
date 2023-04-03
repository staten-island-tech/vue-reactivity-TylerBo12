<script>
export default {
  name: "create",
  components: {},
  data() {
    return {};
  },
  methods: {},
  props: {
    name: String,
    price: String,
  },
};
</script>

<template>
  <div id="parent">
    <div id="container">
      <sub class="child">
        <span class="animals">Item: {{ name }} Price: {{ price }}</span>
        <button>Add to Cart</button>
      </sub>
    </div>
  </div>
</template>

<style scoped>
.child {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  /* --------------------------- */
  margin-right: 5rem;
  margin-top: 2rem;
  width: 28rem;
  border-radius: 1rem;
  background-color: var(--siteBacco);
}

.animals {
  display: flex;
  justify-content: center;
  /* --------------------------- */

  font-size: 3rem;
  margin: 2rem;
  width: 25rem;
  border-radius: 1rem;
  /* --------------------------- */
  border: solid var(--cardBorder) 0.5rem;
  background-color: var(--cardColor);
  color: black;
}
button {
  font-size: 2rem;
}
</style>
