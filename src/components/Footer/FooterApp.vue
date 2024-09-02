<script>
export default {
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
    <div class="container py-5 my-5 border-bottom">
      <div class="row">
        <div class="col-3">
          <div class="content">
            <h4 class="mb-5">
              <img src="../../assets/img/logo-light.png" alt="">
            </h4>
            <ul>
              <li class="py-3 lh-lg" v-for="(label, index) in logo" :key="`logo-${index}`">
                <a :href="label.url" v-html="label.label"></a>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-3">
          <div class="content">
            <h4 class="mb-5">
              Popular Courses
            </h4>
            <ul>
              <li class="py-3 lh-lg" v-for="(label, index) in logo" :key="`logo-${index}`">
                <a :href="label.url" v-html="label.label"></a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;

footer {
  background-color: $a222222;
  color: $ffffff;
  font-size: large;

  a {
    color: white;
  }

  .col-3 {
    .content {
      img {
        width: 60%;
      }

      ;
    }
  }
}
</style>
