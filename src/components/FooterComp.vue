<script>
export default {
  name: "FooterComp",
  data() {
    return {};
  },
};
</script>

<template>
  <div class="foot-j">
    <div class="cont-foot">
      <div class="list">
        <div class="list-l">
          <h3>Dc Comics</h3>
          <ul>
            <li><a href="#">Charcaters</a></li>
            <li><a href="#">Comics</a></li>
            <li><a href="#">Movies</a></li>
            <li><a href="#">Tv</a></li>
            <li><a href="#">Games</a></li>
            <li><a href="#">Videos</a></li>
            <li><a href="#">News</a></li>
          </ul>
          <h3>Shop</h3>
          <ul>
            <li><a href="#">Shop Dc</a></li>
            <li><a href="#">Shop Dc Collectibles</a></li>
          </ul>
        </div>
        <div class="list-c">
          <h3>DC</h3>
          <ul>
            <li><a href="#">Terms Of Use</a></li>
            <li><a href="#">Privacy Policy</a></li>
            <li><a href="#">Ad Choices</a></li>
            <li><a href="#">Adversting</a></li>
            <li><a href="#">Jobs</a></li>
            <li><a href="#">Subscription</a></li>
            <li><a href="#">Talent WorkShops</a></li>
            <li><a href="#">CPSC Certificates</a></li>
            <li><a href="#">Ratings</a></li>
            <li><a href="#">ShopHelp</a></li>
          </ul>
        </div>
        <div class="list-r">
          <h3>SITES</h3>
          <ul>
            <li><a href="#">DC</a></li>
            <li><a href="#">MAD Magazine</a></li>
            <li><a href="#">DC Kids</a></li>
            <li><a href="#">DC Universe</a></li>
            <li><a href="#">DC Power Visa</a></li>
          </ul>
        </div>
      </div>
      <div class="img-foot">
        <img src="../assets/img/dc-logo-bg.png" alt="" />
      </div>
    </div>
  </div>

  <footer>
    <div class="final-foot">
      <div class="cont-btn-foot">
        <a href="#">SIGN-UP-NOW!</a>
      </div>

      <div class="cont-social-foot">
        <h3>Follow Us</h3>

        <a href=""><img src="../assets/img/footer-facebook.png" alt="" /></a>
        <a href=""><img src="../assets/img/footer-twitter.png" alt="" /></a>
        <a href=""><img src="../assets/img/footer-youtube.png" alt="" /></a>
        <a href=""><img src="../assets/img/footer-pinterest.png" alt="" /></a>
        <a href=""><img src="../assets/img/footer-periscope.png" alt="" /></a>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../styles/varibles" as *;
@use "../styles/mixin" as *;

.foot-j {
  width: 100%;
  background-image: url(../assets/img/footer-bg.jpg);
  background-size: cover;
  max-height: 400px;
  overflow: hidden;
  .cont-foot {
    width: 70%;
    height: 100%;
    margin: auto;
    display: flex;
    justify-content: space-between;

    .list {
      display: flex;
      .list-l,
      .list-c,
      .list-r {
        margin: 0px 10px;
        padding-top: 20px;
        h3 {
          color: #fff;
        }
        ul {
          li {
            margin: 10px 0px;
            font-size: 0.8rem;
            a {
              text-decoration: none;
              color: darkgray;
              &:hover {
                color: #fff;
              }
            }
          }
        }
      }
    }
    .img-foot {
      img {
        height: 100%;
        margin-top: -40px;
      }
    }
  }
}
footer {
  height: 100px;
  width: 100%;
  background-color: #303030;
  display: flex;
  align-items: center;
  .final-foot {
    width: 70%;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .cont-btn-foot {
      a {
        text-decoration: none;
        color: white;
        padding: 10px 10px;
        border: 2px solid $primary-color;
      }
    }
    .cont-social-foot {
      @include lowFlex;
      h3 {
        color: $primary-color;
        text-transform: uppercase;
        cursor: pointer;
      }
      img {
        margin: 0px 10px;
      }
    }
  }
}
</style>
