<script>
import ComicCard from './ComicCard.vue';
import comics from '../data/comics';

export default {
  name: 'AppMain',
  components:{
    ComicCard
  },
  data(){
    return{
      comics
    }
  }

}
</script>

<template>
  <main>
    <div class="content cards">
      <ComicCard
      v-for="(comic, index) in comics"
      :key="index"
      :image="comic.thumb"
      :title="comic.series"
      />
      
    </div>
  </main>
  
</template>

<style lang="scss" scoped>
  main{
    // margin: 0 20px;
    padding: 50px;
    min-height: 500px;
    background-color: black;
    color: white;
    font-size: 50px;
    .cards{
      display: flex;
      flex-wrap: wrap;


    }
  }

</style>