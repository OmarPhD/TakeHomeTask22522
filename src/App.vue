<!-- 1 - template tag -->
<template>
  <router-view />
</template>

<!-- 2 - script tag -->
<script></script>

<!-- 3 - style tag -->
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Ubuntu:wght@300;400;500;700&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Ubuntu", sans-serif;
}
body {
  background-color: #333;
}

#app {
  text-align: center;
  color: #fff;
}

.card-shadow {
  -webkit-box-shadow: 0px 5px 5px 0px rgba(8, 8, 8, 0.5);
  -moz-box-shadow: 0px 5px 5px 0px rgba(0, 0, 0, 0.5);
  box-shadow: 0px 5px 5px 0px rgba(0, 0, 0, 0.5);
}
</style>
