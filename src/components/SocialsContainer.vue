<template>
  <div>
    <div class="d-flex justify-content-around text-dark">
      <!--
    <img src="@/assets/GitHub.png" class="avatar" alt="GitHub" />
-->
      <b-container class="shadows-main">
        <h4><a href="https://github.com/garrettHensley" target="_blank"  class="text-dark">GitHub</a></h4>
      </b-container>
      <b-container class="shadows-second">
        <h4><a href="http://garretthensley.me/resume.html" target="_blank" class="text-dark">Resume</a></h4>
      </b-container>
      <b-container class="shadows-second">
        <h4><a href="mailto:garrettmichaelhensley@gmail.com" target="_blank"  class="text-dark">Email</a></h4>
      </b-container>
    </div>
    <p class="my-3 pb-3">
      Feel free to reach out to me, I'm more than happy to answer any questions.
    </p>
  </div>
</template>

<script>
export default {};
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
