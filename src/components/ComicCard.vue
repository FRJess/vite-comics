<script>
export default {
  name: "ComicCard",
  props:{
    card: Object,
  }
};
</script>

<template>

  <div class="card">
    <img :src="card.thumb" alt="card.series">
    <h4>{{card.series}}</h4>
    <p>
      {{ card.price }} <br />
      buy!
    </p>
  </div>
  
</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/mixin" as *;

  .card {
  position: relative;
  width: calc(100% / 6);
  padding: 20px;
  cursor: pointer;
  img {
    width: 150px;
    height: 150px;
    @include image-position();
    transition: 0.5s all;
  }
  h4 {
    color: $white;
    font-size: 0.85rem;
    padding: 5px 0;
    vertical-align: middle;
    display: inline-block;
    text-transform: $text-upper;
  }
  p {
    text-align: center;
    position: absolute;
    top: 30%;
    left: 25%;
    opacity: 0;
    transition: 0.8s all;
    color: $white;
    text-transform: $text-upper;
    font-weight: 600;
    font-size: 0.9rem;
  }
  &:hover p {
    opacity: 1;
  }
  &:hover img {
    filter: brightness(0.4);
  }
}

</style>