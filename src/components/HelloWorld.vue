<template>
  <div v-bind:id="randomId">{{ name }}</div>
</template>

<script>
export default {
  data() {
    return {
      name: "Alsandra",
      randomId: Math.random()
    };
  }
};
</script>

<style>
</style>
