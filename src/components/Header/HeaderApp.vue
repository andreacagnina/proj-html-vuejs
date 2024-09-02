<script>

import HeaderNavbar from './HeaderNavbar.vue';
import HJumbotronCarousel from './HJumbotronCarousel.vue';
export default {
  components: {
    HeaderNavbar,
    HJumbotronCarousel
  },
  data() {
    return {

      navMenu: [
        {
          label: 'home',
          url: '#',
        },
        {
          label: 'courses',
          url: '#',
        },
        {
          label: 'instructors',
          url: '#',
        },
        {
          label: 'events',
          url: '#',
        },
        {
          label: 'pages',
          url: '#',
        },
        {
          label: 'elements',
          url: '#',
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
  </header>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

.z-index {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 2
}
</style>
