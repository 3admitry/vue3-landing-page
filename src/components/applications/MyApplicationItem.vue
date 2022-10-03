<template>
  <div class="col-6 col-md-6 col-xl-3 col mb-4 ">
    <img class="w-100" :src="require(`@/assets/images/${application.filename}`)" alt="">
    <div class="bg-dark text-center text-white py-2">
      {{ application.title }}
    </div>
  </div>
</template>

<script>
export default {
  name: "my-application-item",
  props: {
    application: {
      type: Object,
      required: true,
    }
  }
}
</script>

<style scoped>
</style>