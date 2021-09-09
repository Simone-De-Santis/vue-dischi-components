<template>
  <div class="container mt-5">
    <div class="row row-cols-1 row-cols-md-5 g-4">
      <div v-for="music in collectionMusic" :key="music.author" class="col">
        <div class="card">
          <img :src="music.poster" class="card-img-top" :alt="music.author" />
          <div class="card-body text-center">
            <h5 class="card-title">{{ music.title }}</h5>
            <p class="card-text">
              {{ music.author }}
            </p>
            <p class="card-text">
              {{ music.year }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Main",
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
        console.log(this.collectionMusic[0].author);
      });
  },
};
</script>

<style lang="scss">
</style>