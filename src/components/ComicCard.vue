<script>
export default {
  name: "ComicCard",
  props:{
    image: String,
    price: String,
    title: String,
  }

}
</script>

<template>
  <div class="card">CARD</div>
  
</template>


<style lang="scss" scoped>
  .card{
    flex-basis: 15%;
    min-height: 150px;
  }

</style>