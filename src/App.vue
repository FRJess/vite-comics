<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooterTop from './components/AppFooterTop.vue';
import AppFooterBottom from './components/AppFooterBottom.vue';
import AppBlueMenu from "./components/AppBlueMenu.vue";

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppBlueMenu,
    AppFooterTop,
    AppFooterBottom,
  },

}
</script>

<template>
  <AppHeader/>
  <AppMain/>
  <AppBlueMenu />
  <AppFooterTop/>
  <AppFooterBottom/>
  
</template>

<style lang="scss">
  @use './styles/general';

</style>



<!-- **Descrizione:**
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
**Bonus:**
Creare un componente aggiuntivo per gestire la fascia azzurra con le icone. -->