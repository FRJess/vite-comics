<script>
import menu from '../data/menu';

export default {
  name: 'AppHeader',
  data(){
    return {
      menu
    }
  }
}
</script>

<template>
  <header class="content">

    <div class="logo">
      <img src="../assets/img/dc-logo.png" alt="Logo DC">
    </div>

    <nav>
      <ul>
        <li
        v-for="(link, index) in menu"
        :key="index"
        ><a :class="{'active': link.current}" :href="link.href">{{link.text}}</a></li>
      </ul>
    </nav>
  </header>
  
</template>

<style lang="scss" scoped>

@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

header{
  line-height: 120px;
  @include centerFlex('vertical');
  justify-content: space-between;
  .logo{
    @include centerFlex('vertical');
    img{
      height: 90px;
      cursor: pointer;
    }
  }
  nav{
    ul{
      height: 100%;
      list-style-type: none;
      margin: 0 auto;
      @include centerFlex('both');
      li{
        margin: 0 10px 0 10px;
        @include centerFlex('vertical');
      }
      a{
        text-decoration: none;
        color: $primary-color;
        text-transform: $text-upper;
        &:hover {
          color: $dc-color;
        }
        &.active {
          color: $dc-color;
          box-shadow: inset 0 -7px 0 $dc-color;
        }
      }
  
    }
  }
}

</style>