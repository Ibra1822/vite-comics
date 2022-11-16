<script>
export default {
  name: "JumboComp",

  data() {
    return {
      jumboPic: "jumbotron.jpg",
    };
  },
  methods: {
    getImg(imgName) {
      return new URL(`../assets/img/${imgName}`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <div class="jumbotron">
    <img :src="getImg(jumboPic)" alt="" />
  </div>
  <button>Current Series</button>
</template>

<style lang="scss" scoped>
@use "../styles/mixin" as *;
.jumbotron {
  height: 380px;
  background-color: cadetblue;

  img {
    height: 100%;
    width: 100%;
    object-fit: cover;
    object-position: 90% 0%;
    position: relative;
  }
}
button {
  @include myButton;
  position: absolute;
  transform: translate(-50%, -50%);
  left: 23%;
  font-size: 1.1rem;
}
</style>
