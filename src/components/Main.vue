<template>
  <div class="container mt-5">
    <div class="row row-cols-1 row-cols-md-5 g-4">
      <Card
        v-for="(music, index) in collectionMusic"
        :key="index"
        class="col"
        :poster="music.poster"
        :author="music.author"
        :title="music.title"
        :year="music.year"
      />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Card from "./Card.vue";
export default {
  name: "Main",
  components: {
    Card,
  },
  data() {
    return {
      collectionMusic: [],
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        this.collectionMusic = res.data.response;
        console.log(this.collectionMusic);
      });
  },
};
</script>

<style lang="scss">
</style>