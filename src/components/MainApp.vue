<script>
import MCardSection from './MCardSection.vue';
import MFirstSection from './MFirstSection.vue';
import MSecondSection from './MSecondSection.vue';
import MThirdSection from './MThirdSection.vue';

export default {
  components: {
    MCardSection,
    MFirstSection,
    MSecondSection,
    MThirdSection,
  }

}
</script>

<template>

  <MCardSection />
  <MFirstSection />
  <MSecondSection />
  <MThirdSection />

</template>

<style lang="scss" scoped>
@use '../styles/partials/Colors' as*;
</style>
