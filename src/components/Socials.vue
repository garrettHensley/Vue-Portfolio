<template>
  <div class="fixed d-none d-xl-block">
    <img src="@/assets/GitHub.png" class="avatar" alt="GitHub" />
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
