<template>
  <div class="home">
    <!-- render any given components -->
    <navbar />
    <div id="main-section">
      <album-list />
    </div>
  </div>
</template>

<script>
// add navbar/header component
import Navbar from "../components/Navbar.vue";
import AlbumList from "../components/AlbumList.vue";

export default {
  name: "HomeView",
  components: {
    Navbar,
    AlbumList,
  },
};
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  flex-direction: column;

  #main-section {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 50px;
  }
}
</style>
