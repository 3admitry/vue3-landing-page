<template>
  <div class="main-banner__content vh-100 d-flex justify-content-center align-items-center">
    <div class="text-white text-center">
      <h1 class="display-1 fw-bold">Welcome to Test Page</h1>
      <span class="fs-1">Front-end developer</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainPhoto"
}
</script>

<style scoped lang="scss">
.main-banner {
  &__content {
    background-image: url("@/assets/images/bg_main.jpg");
    background-size: cover;
  }
}
</style>