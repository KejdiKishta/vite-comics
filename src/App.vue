<!-- **Descrizione:**
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass! -->
<!-- **Bonus:**
Creare un componente aggiuntivo per gestire la fascia azzurra con le icone. -->

<script>
import AppHeader from './components/AppHeader.vue';
import AppJumbotron from './components/AppJumbotron.vue';
import AppMain from './components/AppMain.vue';
import AppNav from './components/AppNav.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppJumbotron,
    AppMain,
    AppNav,
    AppFooter
  },

  data() {
    return {
      
    }
  }
}
</script>

<template>

  <!-- header -->
  <AppHeader />

<!-- jumbotron -->
  <AppJumbotron />

  <!-- main -->
  <AppMain />

  <!-- nav -->
  <AppNav />

  <!-- footer -->
  <AppFooter />
  
</template>

<style scoped lang="scss">

</style>
