<template>
  <div>
    <div class="d-flex justify-content-around text-dark">
      <template v-for="link in links">
        <b-button
          :href="link.href"
          target="_blank"
          :key="link.name"
          block
          variant="bg-second"
          class="shadows-second"
        >
          <h4>{{link.name}}</h4>
        </b-button>
      </template>
    </div>
    <p class="my-3 pb-3">Feel free to reach out to me, I'm more than happy to answer any questions.</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        { name: "GitHub", href: "https://github.com/garrettHensley" },
        { name: "Resume", href: "http://garretthensley.me/resume.html" },
        { name: "Email", href: "mailto:garrettmichaelhensley@gmail.com" }
      ]
    };
  }
};
</script>

<style scoped>
.avatar {
  background-color: #e9e9e0;
  border-radius: 50%;
  border: 0.1rem solid #e9e9e0;
  box-shadow: 0.2rem 0.2rem 16px rgb(40, 42, 61, 0.6),
    -0.2rem -0.2rem 16px rgba(233, 233, 224, 0.7);
}

.fixed {
  position: absolute;
  top: 19em;
  left: 75em;
  z-index: 2;
}
</style>
