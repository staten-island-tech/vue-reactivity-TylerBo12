<script>
export default {
  data() {
    return {
      array: [
        { name: "anteater", foods: "ant", status: "predator" },
        { name: "arctic bear", foods: "feesh", status: "predator" },
      ],
    };
  },
};
</script>

<template>
  <div v-for="animals in array" :key="animals.name" class="Pain">
    {{ animals.name }}
  </div>
  <h1>Henlo</h1>
</template>

<style scoped>
.Pain {
  font-size: 10rem;
  background-color: aqua;
}
</style>
