<script>
export default {
  data() {
    return {
      text: `Trooooll `,
      hehe: `trolling`,
      count: 0,
    };
  },
  methods: {
    decrement() {
      this.count--;
    },
  },
};
</script>

<template>
  <h1 v-bind:class="hehe">{{ text }}</h1>
  <h1>
    <button @click="decrement">`Click This`</button>
  </h1>
</template>

<style scoped>
h1 {
  font-size: 5rem;
  color: green;
}

button {
}

.trolling {
  color: red;
}
</style>
