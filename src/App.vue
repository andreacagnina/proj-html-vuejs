<script>
import HeaderApp from './components/Header/HeaderApp.vue'
import MainApp from './components/Main/MainApp.vue'
import FooterApp from './components/Footer/FooterApp.vue'
export default {
  components: {
    HeaderApp,
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
@use './styles/partials/Colors' as*;

/* width */
::-webkit-scrollbar {
  width: 10px;
  height: 10px;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: $a9ce0ff;
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: $a40c4ff;
  cursor: pointer;
}
</style>
