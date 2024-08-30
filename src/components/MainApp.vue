<script>
import CardSection from './CardSection.vue';
export default {
  components: {
    CardSection,
  }

}
</script>

<template>
  <div class="container my-5">
    <div class="row">
      <CardSection />
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/Colors' as*;
</style>
