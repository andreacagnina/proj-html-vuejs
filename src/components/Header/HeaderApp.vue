<script>

import HeaderNavbar from './HeaderNavbar.vue';
import HeaderOffcanvas from './HeaderOffcanvas.vue';
import HJumbotronCarousel from './HJumbotronCarousel.vue';
export default {
  components: {
    HeaderNavbar,
    HJumbotronCarousel,
    HeaderOffcanvas,
  },
  data() {
    return {

      navMenu: [
        {
          label: 'home',
          url: '#',
          id: '#1'
        },
        {
          label: 'courses',
          url: '#',
          id: '#2'
        },
        {
          label: 'instructors',
          url: '#',
          id: '#3'
        },
        {
          label: 'events',
          url: '#',
          id: '#4'
        },
        {
          label: 'pages',
          url: '#',
          id: '#5'
        },
        {
          label: 'elements',
          url: '#',
          id: '#6'
        }
      ]
    };
  },
}
</script>

<template>
  <header>
    <headerNavbar :navMenu="navMenu" class="z-index p-5" />
    <HJumbotronCarousel />
    <HeaderOffcanvas />
  </header>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

.z-index {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1
}
</style>
