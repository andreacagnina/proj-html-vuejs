<script>
import MCardSection from './MCardSection.vue';
import MFirstSection from './MFirstSection.vue';
import MSecondSection from './MSecondSection.vue';
import MThirdSection from './MThirdSection.vue';
import MFourthSection from './MFourthSection.vue';
import MFifthSection from './MFifthSection.vue';
import MSixthSection from './MSixthSection.vue';

export default {
  components: {
    MCardSection,
    MFirstSection,
    MSecondSection,
    MThirdSection,
    MFourthSection,
    MFifthSection,
    MSixthSection
  }

}
</script>

<template>

  <MCardSection />
  <MFirstSection />
  <MSecondSection />
  <MThirdSection />
  <MFourthSection />
  <MFifthSection />
  <MSixthSection />

</template>

<style lang="scss" scoped>
@use '../../styles/partials/Colors' as*;
</style>
