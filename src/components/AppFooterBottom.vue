<script>
export default {
  name: 'AppFooterBottom',

}
</script>

<template>
  <footer>

    <div class="container">
      <div>
        <button>Sign-up now</button>
      </div>
    </div>
  
  </footer>

</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;
footer{
  background-color: $primary-color;
  height: 200px;
}


</style>

