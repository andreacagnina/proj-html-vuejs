<script>

import HeaderNavbar from './HeaderNavbar.vue';
export default {
  components: {
    HeaderNavbar
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
  <header class="p-5">
    <headerNavbar :navMenu="navMenu" />
  </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/Colors' as*;
</style>
