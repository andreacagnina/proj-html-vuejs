<script>
import HeaderApp from './components/HeaderApp.vue'
import Carousel from './components/Carousel.vue';
import MainApp from './components/MainApp.vue'
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
  <HeaderApp class="zindex" />
  <Carousel />
  <MainApp />
  <FooterApp />
</template>

<style lang="scss">
@use './styles/generals.scss';


.zindex {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1
}
</style>
