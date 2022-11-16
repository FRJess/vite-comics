<script>
import ComicCard from './ComicCard.vue';
import cards from '../data/comics';

export default {
  name: 'AppMain',
  components:{
    ComicCard,
  },
  data(){
    return{
      cards,
    }
  }
};

</script>

<template>
  <main>
    <div class="jumbotron">
      <img src="../assets/img/jumbotron.jpg" alt="jumbotron" />
    </div>
    <h2 class>Current series</h2>
    <div class="content">
      
      <ComicCard
      v-for="(card, index) in cards"
      :key="index"
      :card="card"
      />
      
    </div>
    <button>Load more</button>
  </main>
  
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixin" as *;

  main{
    padding-bottom: 10px;
    background-color: $primary-color;
    color: $white;
      h2 {
        width: 215px;
        transform: translateY(-50%);
        margin-left: 6%;
        text-align: center;
        color: $white;
        text-transform: $text-upper;
        padding: 8px;
        background-color: $dc-color;
        border: 1px solid $primary-color;
      }
      .jumbotron img {
        height: 400px;
        width: 100%;
        @include image-position();
      }
      .content {
        @include centerFlex('wrap');
      }
      button{
        margin: 0 auto;
        display: block;
        @include button();
      }
  }

</style>