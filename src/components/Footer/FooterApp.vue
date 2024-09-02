<script>
import FBottomBar from './FBottomBar.vue';
import FMenu from './FMenu.vue';
export default {
  components: {
    FMenu,
    FBottomBar,
  },
  data() {
    return {
      logo: [
        {
          label: 'Providing Life Changing Experiences Through Education. Class That Fit Your Busy Life. Closer to Home',
          url: '#',
        },
        {
          label: '<i class="fa-solid fa-phone-volume"></i>&nbsp; 1-677 - 124 - 44227',
          url: '#'
        },
        {
          label: '<i class="fa-regular fa-clock"></i>&nbsp; Mon - Sat 8.00 - 18.00',
          url: '#',
        }
      ],
      PopularCourses: [
        {
          matter: 'Business English',
          teacher: 'Preston Marshall',
        },
        {
          matter: 'Social Computing',
          teacher: 'David Sanders',
        },
        {
          matter: 'Learn Spanish',
          teacher: 'Jennie King',
        }
      ],
      support: [
        {
          label: 'User dashboard',
          url: '#',
        },
        {
          label: 'Contact Us',
          url: '#',
        },
        {
          label: 'FAQ',
          url: '#',
        },
        {
          label: 'Course Offer',
          url: '#',
        },
        {
          label: 'Events',
          url: '#',
        },
      ],
    }
  }
}
</script>

<template>
  <footer class="py-5">
    <FMenu :logo="logo" :PopularCourses="PopularCourses" :support="support" />
    <FBottomBar />
  </footer>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

footer {
  background-color: $a222222;
  color: $ffffff;
  font-size: large;

}
</style>
