<script>
import MCardSection from './MCardSection.vue';
import MFirstSection from './MFirstSection.vue';
import MSecondSection from './MSecondSection.vue';

export default {
  components: {
    MCardSection,
    MFirstSection,
    MSecondSection,
  }

}
</script>

<template>

  <MCardSection />
  <MFirstSection />
  <MSecondSection />

</template>

<style lang="scss" scoped>
@use '../styles/partials/Colors' as*;
</style>
