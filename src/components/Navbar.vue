<template>
  <div id="navbar-wrap" class="card-shadow">
    <div id="navbar">
      <h1>Album Search</h1>
      <div style="padding: 50px 0">
        <input v-model="search" type="text" placeholder="search song" />
        <!-- fontawesome cdn for magnifying glass img -->
        <!-- <font-awesome-icon icon="fa-solid fa-magnifying-glass" /> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search: "",
    };
  },
  watch: {
    search() {
      this.$store.dispatch("search", this.search);
    },
  },
};
</script>

<style lang="scss" scoped>
#navbar-wrap {
  width: 100%;

  #navbar {
    display: flex;
    padding: 100px;
    flex-direction: column;
    justify-content: space-between;
    background-color: #273c75;

    h1 {
      color: #fff;
    }

    input {
      width: 50%;
      border: none;
      height: 25px;
      border-radius: 5px;
      box-sizing: border-box;
      outline: none;
      padding: 20px;
    }
  }
}
</style>
