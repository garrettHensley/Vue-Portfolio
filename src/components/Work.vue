<template>
  <div class="mb-3">
    <SectionHeader section="Projects & Apps" />
    <JobContainer />
  </div>
</template>

<script>
import JobContainer from "@/components/JobContainer.vue";
import SectionHeader from "@/components/SectionHeader.vue";

export default {
  components: {
    JobContainer,
    SectionHeader
  }
};
</script>
