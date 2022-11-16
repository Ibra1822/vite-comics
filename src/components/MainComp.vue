<script>
import CardComp from "./CardComp.vue";
import arrayComp from "../data/Array";
export default {
  name: "MainComp",
  components: {
    CardComp,
  },
  data() {
    return {
      arrayComp,
    };
  },
};
</script>

<template>
  <main>
    <div class="content">
      <CardComp v-for="(item, index) in arrayComp" :key="index" :ogt="item" />
      <button>Load More</button>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../styles/varibles" as *;

main {
  max-width: 100%;
  background-color: #1c1c1c;
  .content {
    width: 70%;
    display: flex;
    align-items: center;
    flex-wrap: wrap;
    margin: auto;
    padding: 20px;
    button {
      margin: 30px auto;
      padding: 10px 55px;
      border: 0px;
      color: #fff;
      background-color: $primary-color;
      font-weight: 500;
      text-transform: uppercase;
      cursor: pointer;
    }
    h2 {
      color: white;
    }
  }
}
</style>
