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
    <div class="content">
      
      <ComicCard
      v-for="(card, index) in cards"
      :key="index"
      :card="card"
      />
      
    </div>
  </main>
  
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixin" as *;

  main{
    // margin: 0 20px;
    padding: 50px;
    min-height: 500px;
    background-color: black;
    color: white;
    font-size: 50px;
      .content {
        display: flex;
        flex-wrap: wrap;
    }
  }

</style>