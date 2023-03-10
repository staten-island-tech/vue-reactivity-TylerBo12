<script>
import { ref } from "vue";
let counter = 0;

const newTodo = ref(``);

export default {
  data() {
    return {
      text: `Hey you, yes you, have a bad day. :(`,
      fontColor: `color`,
      count: 0,
      yes: true,
    };
  },
  methods: {
    decrement() {
      this.count--;
    },
    toggle() {
      this.yes = !this.yes;
    },
  },
};
</script>

<template>
  <h1 v-bind:class="fontColor">{{ text }}</h1>
  <h1>
    <button @click="decrement">Amount of friends you have: {{ count }}</button>
  </h1>

  <button @click="toggle">Tell me</button>
  <h1 v-if="yes">Damn you hate life too.</h1>
  <h1 v-else>I guess you have a good schedule</h1>
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

button {
  font-size: 4rem;
}
</style>
