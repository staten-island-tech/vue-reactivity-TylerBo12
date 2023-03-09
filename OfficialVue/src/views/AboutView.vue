<script>
export default {
  data() {
    return {
      text: `Hey you, yes you, have a bad day. :(`,
      fontColor: `color`,
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
  <h1 v-bind:class="fontColor">{{ text }}</h1>
  <h1>
    <button @click="decrement">Amount of friends you have: {{ count }}</button>
  </h1>
</template>

<style scoped>
h1 {
  font-size: 5rem;
  width: 50rem;
  height: 8rem;
  color: green;
}

.color {
  color: red;
}
</style>
