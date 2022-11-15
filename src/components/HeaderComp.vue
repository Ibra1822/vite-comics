<script>
export default {
  name: "HeaderComp",
  data() {
    return {
      menu: [
        {
          title: "Charcaters",
          href: "#",
          active: false,
        },
        {
          title: "Comics",
          href: "#",
          active: true,
        },
        {
          title: "Movies",
          href: "#",
          active: false,
        },
        {
          title: "Tv",
          href: "#",
          active: false,
        },
        {
          title: "Games",
          href: "#",
          active: false,
        },
        {
          title: "Collectibles",
          href: "#",
          active: false,
        },
        {
          title: "Videos",
          href: "#",
          active: false,
        },
        {
          title: "Fans",
          href: "#",
          active: false,
        },
        {
          title: "News",
          href: "#",
          active: false,
        },
        {
          title: "Shop",
          href: "#",
          active: false,
        },
      ],

      headerLogo: "dc-logo.png",
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
  <header class="debug">
    <div class="cont-all">
      <div class="cont-img">
        <img :src="getImg(headerLogo)" alt="" />
      </div>
      <div class="cont-link">
        <ul>
          <li v-for="(link, index) in menu" :key="index">
            <a
              :class="{ active: link.active }"
              @click="link.active = !link.active"
              :href="link.href"
              >{{ link.title }}</a
            >
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../styles/varibles" as *;
@use "../styles/mixin" as *;

.active {
  border-bottom: 3px solid $primary-color;
}

header {
  height: 120px;
  width: 100%;
  @include lowFlex;
  .cont-all {
    width: 70%;
    margin: 0 auto;
    @include advancedFlex;
    img {
      height: 70px;
    }
  }

  .cont-link {
    ul {
      @include baseFlex;
      list-style: none;
      li {
        margin: 0 10px;
        a {
          color: black;
          text-decoration: none;
          font-weight: 500;
          padding: 49px 0px;
          text-transform: uppercase;
          &:hover {
            color: $primary-color;
          }
        }
      }
    }
  }
}
</style>
