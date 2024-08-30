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
  <header class="p-4">
    <div class="container-fluid">
      <div class="row">
        <div class="col-12 bg-dark">
          <div class="d-flex justify-content-between align-items-baseline">
            <div class="content">
              <a href="#">
                <img src="../assets/img/logo-light.png" alt="logo">
              </a>
            </div>
            <div class="content">
              <ul>
                <li v-for="(label, index) in HeaderMenu" :key="`HM-${index}`"><a class="fw-bold" :href="label.url">{{
                  label.label }}</a></li>
              </ul>
            </div>
            <div class="content">
              <ul>
                <li><a href="#"><i class="fa-solid fa-magnifying-glass fa-rotate-90"></i></a>
                </li>
                <li><a href="#"><i class="fa-solid fa-bag-shopping"></i></a></li>
                <li><a href="#"><i class="fa-solid fa-bars"></i></a></li>

              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/bgColors' as*;
@use '../styles/partials/borderColors' as*;
@use '../styles/partials/fillColors' as*;
@use '../styles/partials/textColors' as*;

img {
  width: 60%;
}

ul {
  display: flex;

  li {
    display: flex;
    align-items: center;
    padding: 0 30px;
  }

  a {
    text-transform: uppercase;
    color: white;
  }
}
</style>
