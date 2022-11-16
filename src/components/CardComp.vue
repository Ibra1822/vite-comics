<script>
export default {
  name: "CardComp",
  props: {
    ogt: Object,
  },
};
</script>

<template>
  <div class="cont-big-card">
    <div class="cont-img">
      <img :src="ogt.thumb" :alt="ogt.series" />
    </div>

    <div class="cont-text">
      <p>{{ ogt.series }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.cont-big-card {
  height: 200px;
  width: calc(100% / 6);
  padding: 10px;
  margin-bottom: 10px;
  .cont-img {
    height: 90%;
    width: 100%;
    cursor: pointer;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: 90% 0%;
    }
  }
}

.cont-text {
  cursor: pointer;
  padding: 10px 0px;
  p {
    color: #fff;
    font-size: 0.8rem;
  }
}
</style>
