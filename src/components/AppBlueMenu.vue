<script>
import menu from '../data/blue-menu.js';

export default {
  name: 'AppBlueMenu',
  data(){
    return {
      menu,
    }
  },

  methods: {
    getPathImage(imageName) {
      return new URL(`../assets/img/${imageName}`, import.meta.url).href;
    },
  },
};
</script>

<template>
  <div class="menu-box">
    <div class="content">
      <ul>
        <li 
        v-for="(link, index) in menu" 
        :key="index">
          <img :src="getPathImage(link.img)" :alt="link.text" />
          <a href="#">{{ link.text }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/general.scss" as *;
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixin" as *;
.menu-box {
  background-color: $dc-color;
  .content {
    ul {
      justify-content: space-between;
      @include centerFlex('horizontal');
      li {
        @include centerFlex('vertical');
        img {
          transform: scale(0.5);
        }
        a {
          text-decoration: none;
          color: $white;
          font-size: 0.9rem;
          text-transform: $text-upper;
        }
      }
    }
  }
}
</style>