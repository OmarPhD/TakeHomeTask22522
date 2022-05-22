<template>
  <div class="album">
    <img :src="album.poster" alt="Album poster" />
    <div class="description">
      <div class="basic-info">
        <h3>{{ album.name }}</h3>
      </div>
      <p>{{ album.genre }}</p>
      <p>{{ album.year }}</p>
    </div>
  </div>
</template>

<script>
import { objectExpression } from "@babel/types";

export default {
  props: {
    album: {
      type: objectExpression,
      default: () => {},
    },
  },
};
</script>

<style lang="scss" scoped>
.album {
  flex: 1;
  margin: 1rem;
  min-width: 300px;
  max-width: 300px;
  position: relative;

  img {
    max-width: 100%;
    box-shadow: 0 14px 28px rgba(0, 0, 0, 0.473),
      0 10px 10px rgba(0, 0, 0, 0.473);
    margin-bottom: 7px;
    border-radius: 15px;
    cursor: pointer;
  }

  .description {
    padding: 1rem 0;

    .basic-info {
      text-align: center;
      h3 {
        margin: 0;
        text-align: center;
        color: white;
      }

      span {
        border-radius: 10px;
        font-size: 20px;
        width: 53px;
        color: white;
      }
    }

    p {
      margin: 5px 0;
      color: rgb(143, 143, 143);
      text-align: center;
    }
  }
}
</style>
