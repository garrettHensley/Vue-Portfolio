<template>
  <div>
    <SectionHeader section="About Me" />
    <AboutContainer />
  </div>
</template>

<script>
import SectionHeader from "@/components/SectionHeader.vue";
import AboutContainer from "@/components/AboutContainer.vue";

export default {
  components: {
    SectionHeader,
    AboutContainer
  }
};
</script>