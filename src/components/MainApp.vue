<script>
import MCardSection from './MCardSection.vue';
import MFirstSection from './MFirstSection.vue';
export default {
  components: {
    MCardSection,
    MFirstSection
  }

}
</script>

<template>

  <MCardSection />
  <MFirstSection />

</template>

<style lang="scss" scoped>
@use '../styles/partials/Colors' as*;
</style>
