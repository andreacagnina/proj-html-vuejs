<script>
import HeaderApp from './components/Header/HeaderApp.vue'
//import Carousel from './components/Header/Carousel.vue';
import MainApp from './components//Main/MainApp.vue'
import FooterApp from './components/FooterApp.vue'
export default {
  components: {
    HeaderApp,
    //Carousel,
    MainApp,
    FooterApp
  }
}
</script>

<template>
  <HeaderApp />
  <MainApp />
  <FooterApp />
</template>

<style lang="scss">
@use './styles/generals.scss';
</style>
