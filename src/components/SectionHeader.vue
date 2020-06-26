<template>
  <b-container class="bg-main  shadows-main mb-3">
    <h1>{{ section }}</h1>
  </b-container>
</template>

<script>
export default {
  props: {
    section: String,
  },
};
</script>

<style scoped></style>
