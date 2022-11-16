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
@use "../styles/mixin" as *;

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
      @include myButton;
    }
    h2 {
      color: white;
    }
  }
}
</style>
