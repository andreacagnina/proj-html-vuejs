<script>
import HeaderApp from './components/Header/HeaderApp.vue'
import Carousel from './components/Header/Carousel.vue';
import MainApp from './components//Main/MainApp.vue'
import FooterApp from './components/FooterApp.vue'
export default {
  components: {
    HeaderApp,
    Carousel,
    MainApp,
    FooterApp
  }
}
</script>

<template>
  <HeaderApp class="z-index" />
  <Carousel />
  <MainApp />
  <FooterApp />
</template>

<style lang="scss">
@use './styles/generals.scss';


.z-index {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1
}

h1 {
  font-size: 5rem;
}

h2 {
  font-size: 3rem;
}
</style>
