<template>
  <div class="card">
    <img :src="poster" class="card-img-top" />

    <div class="card-body text-center">
      <h5 class="card-title">{{ author }}</h5>

      <p class="card-text">
        {{ author }}
      </p>
      <p class="card-text">
        {{ author }}
      </p>
    </div>
    <h1></h1>
  </div>
</template>

<script>
export default {
  name: "Card",
  data() {},
  props: {
    poster: String,
    author: String,
    title: String,
    year: String,
  },
};
</script>

<style>
</style>