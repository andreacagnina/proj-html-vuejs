<script>
import { HeaderMenu } from '../data/HeaderMenu';
export default {
  data() {
    return {
      HeaderMenu
    }
  }
}
</script>

<template>
  <header class="p-5">
    <div class="container-fluid">
      <div class="row">
        <div class="col-12">
          <div class="d-flex justify-content-between align-items-baseline">
            <div class="content">
              <a href="#">
                <img src="../assets/img/logo-light.png" alt="logo">
              </a>
            </div>
            <div class="content">
              <ul>
                <li class="px-5" v-for="(label, index) in HeaderMenu" :key="`HM-${index}`"><a :href="label.url">{{
                  label.label }}</a></li>
              </ul>
            </div>
            <div class="content">
              <ul>
                <li><a href="#"><i class="fa-solid fa-magnifying-glass fa-rotate-90 fa-xl"></i></a>
                </li>
                <li><a href="#"><i class="fa-solid fa-bag-shopping fa-xl position-relative"><span class="position-absolute bottom-100 start-50
                  badge rounded-pill bg-badge fs-6">
                        0</span></i></a></li>
                <li><a href="#"><i class="fa-solid fa-bars fa-xl"></i></a></li>

              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/Colors' as*;

img {
  width: 200px;
}


ul {
  display: flex;

  li {
    display: flex;
    align-items: center;
    margin: 0 20px;
  }

  a {
    text-transform: uppercase;
    color: $ffffff;
    font-size: larger;

  }
}

.bg-badge {
  background-color: $a40c4ff;
}
</style>
