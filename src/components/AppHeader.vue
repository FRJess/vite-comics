<script>
export default {
  name: 'AppHeader',
  data(){
    return{
      menu:[
        {
          text: 'Characters',
          href: '#',
          current: false,
        },
        {
          text: 'Comics',
          href: '#',
          current: true,
        },
        {
          text: 'Movies',
          href: '#',
          current: false,
        },
        {
          text: 'TV',
          href: '#',
          current: false,
        },
        {
          text: 'Games',
          href: '#',
          current: false,
        },
        {
          text: 'Collectibles',
          href: '#',
          current: false,
        },
        {
          text: 'Videos',
          href: '#',
          current: false,
        },
        {
          text: 'Fans',
          href: '#',
          current: false,
        },
        {
          text: 'News',
          href: '#',
          current: false,
        },
        {
          text: 'Shop',
          href: '#',
          current: false,
        },
    
      ]
    }
  }
}
</script>

<template>
  <header class="container">

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
  height: 180px;
  display: flex;
  justify-content: space-between;
  text-align: center;
  .logo{
    margin: auto 0;
  }
  nav{
    margin: auto 0;
    ul{
      margin-top: 20px;
      list-style-type: none;
      @include centerFlex('horizontal');
      a{
        text-decoration: none;
        display: inline-block;
        padding: 1rem;
        color: #464646;
        text-transform: uppercase;
        font-weight: 600;
      }
  
    }
  }
}

</style>