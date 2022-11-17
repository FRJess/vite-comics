<script>
export default {
  name: "AppFooterBottom",
};
</script>

<template>
  <footer>
    <div class="content">
      <h4>Sign-up now!</h4>
      <div class="follow-us">
        <h4>Follow us</h4>
        <img src="../assets/img/footer-facebook.png" alt="facebook" />
        <img src="../assets/img/footer-twitter.png" alt="twitter" />
        <img src="../assets/img/footer-youtube.png" alt="youtube" />
        <img src="../assets/img/footer-pinterest.png" alt="pinterest" />
        <img src="../assets/img/footer-periscope.png" alt="periscope" />
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/general.scss" as *;
@use "../styles/partials/mixin" as *;

footer {
  height: 110px;
  background-color: lighten($primary-color, 8%);
  .content {
    @include centerFlex('vertical');
    justify-content: space-between;
    height: 100%;
    & > h4 {
      margin-left: 40px;
      padding: 13px;
      border: 2px solid $dc-color;
      color: $white;
      cursor: pointer;
      text-transform: $text-upper;
    }
    .follow-us {
      display: flex;
      img {
        margin: 0 7px;
        cursor: pointer;
      }
      & > h4 {
        color: $dc-color;
        margin-right: 30px;
        padding-top: 5px;
        font-size: 1.1rem;
        text-transform: $text-upper;
        font-weight: 600;
        cursor: pointer;
      }
    }
  }
}
</style>