<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooterTop from './components/AppFooterTop.vue';
import AppFooterBottom from './components/AppFooterBottom.vue';
import AppBlueMenu from './components/AppBlueMenu.vue';
import ComicCard from './components/ComicCard.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppBlueMenu,
    AppFooterTop,
    AppFooterBottom,
    ComicCard,
  },

}
</script>

<template>
  <AppHeader/>
  <AppMain/>
  <AppBlueMenu />
  <AppFooterTop/>
  <AppFooterBottom/>
  <!-- <ComicCard :card=""/> -->
  
</template>

<style lang="scss">
  @use './styles/general';

</style>



<!-- **Descrizione:**
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
**Bonus:**
Creare un componente aggiuntivo per gestire la fascia azzurra con le icone.

Continuate a lavorare nella stessa repo di ieri e create un nuovo componente per visualizzare le card dei fumetti, prendendo i dati dal file json che trovate in allegato.
Una volta inseriti tutti i contenuti dinamicamente, completate il vostro layout e rifinite i dettagli con Sass.
In base a come vi è più comodo stabilite dove mettere l’array dei dati per poi passere le props alle card -->