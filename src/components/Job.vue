<template id="job" class="bg-second border">
  <b-container id="job" class="text-light">
    <p class="lead">
      {{ name }}
    </p>
    <img :src="image" class="img-fluid d-none d-lg-block" />
    <p class="lead"><a :href="link" target="_blank">{{ link }}</a></p>
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
p {
  word-wrap: break-word;
}
</style>
