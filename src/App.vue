<script>
import HeaderComp from "./components/HeaderComp.vue";
import MainComp from "./components/MainComp.vue";
import FooterComp from "./components/FooterComp.vue";
import IconsCenter from "./components/IconsCenter.vue";
import JumboComp from "./components/JumboComp.vue";
export default {
  name: "App",

  components: {
    HeaderComp,
    MainComp,
    FooterComp,
    IconsCenter,
    JumboComp,
  },
};
</script>

<template>
  <HeaderComp />
  <JumboComp />
  <MainComp />
  <icons-center />
  <FooterComp />
</template>

<style lang="scss">
@use "./styles/general.scss";
</style>
