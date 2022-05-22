<template>
  <!-- style="display: flex;align-items: center;justify-content: center; height: 100vh; width: 100%;" -->
  <div id="album-container">
    <album v-for="album in albums" :key="album.id" :album="album" />
  </div>
</template>

<script>
import Album from "./Album.vue";

export default {
  components: {
    Album,
  },
  data() {
    return {
      albums: [],
    };
  },

  computed: {
    albums() {
      return this.$store.getters.getAlbums;
    },
  },
};
</script>

<style lang="scss" scoped>
#movie-container {
  padding-top: 1rem;
  display: flex;
  flex-wrap: wrap;
  flex-grow: 1;
  justify-content: center;
}
</style>
