<script>
export default {
  array: [{ name: "anteater", foods: "ant", status: "predator" }],
};
</script>

<template>
  <p v-for="animals in array" class="Pain">{{ animals.text }}</p>
</template>

<style scoped>
.Pain {
  font-size: 10rem;
}
</style>
