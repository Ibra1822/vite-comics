<script>
export default {
  name: "IconsCenter",
  data() {
    return {
      ogt: [
        {
          desc: "Digital Comics",
          img: "buy-comics-digital-comics.png",
        },
        {
          desc: "DC MERCHANDISE",
          img: "buy-comics-merchandise.png",
        },
        {
          desc: "SUBSCRIPTION",
          img: "buy-comics-subscriptions.png",
        },
        {
          desc: "COMIC SHOP LOCATOR",
          img: "buy-comics-shop-locator.png",
        },
        {
          desc: "DC POWER VISA",
          img: "buy-dc-power-visa.svg",
        },
      ],
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
  <div class="cont-icons">
    <ul>
      <li v-for="(item, index) in ogt" :key="index" class="item-blue">
        <a href="">
          <img :src="getImg(item.img)" :alt="item.desc" />
          <h5>{{ item.desc }}</h5>
        </a>
      </li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/varibles" as *;
@use "../styles/mixin" as *;

.cont-icons {
  width: 100%;
  background-color: $primary-color;
  ul {
    height: 100%;
    width: 70%;
    margin: auto;
    display: flex;
    justify-content: space-evenly;
    li {
      padding: 50px 0px;
      a {
        height: 100%;
        @include baseFlex;
        align-items: center;
        text-decoration: none;
        img {
          height: 50px;
        }
        h5 {
          color: #fff;
          margin: 0px 10px;
        }
      }
    }
  }
}
</style>
