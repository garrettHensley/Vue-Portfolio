<template id="job" class="bg-second border">
  <b-container id="job" class="text-light">
    <p class="h1 py-3">{{ app.name }}</p>
    <img :src="app.img" class="img-fluid d-none d-lg-block" />
    <p class="lead d-flex justify-content-around pt-3">
      <b-button
        variant="primary"
        v-b-tooltip.hover
        :title="'Take a look at the codebase for ' + app.name "
        :href="app.source"
        target="_blank"
      >Codebase</b-button>
      <b-button
        v-if="app.pages"
        variant="primary"
        v-b-tooltip.hover
        :title="'Here\'s a sneak peek of ' + app.name"
        :href="app.pages"
        target="_blank"
      >Demo</b-button>
    </p>
    <p class="lead">{{ app.description }}</p>
  </b-container>
</template>

<script>
export default {
  props: {
    app: Object
  }
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
