<template id="job" class="bg-second border">
  <b-container id="job" class="text-light">
    <p class="lead">
      {{ name }}
    </p>
    <img :src="image" class="img-fluid" />
    <p>{{ link }}</p>
    <p class="lead">{{ description }}</p>
  </b-container>
</template>

<script>
export default {
  props: {
    name: String,
    description: String,
    link: String,
    image: String,
    pages: String,
  },
  methods: {
    getUrl() {
      return this.name.replace(" ", "");
    },
  },
};
</script>

<style scoped>
#job {
  background-color: #282a3d;
}
</style>
