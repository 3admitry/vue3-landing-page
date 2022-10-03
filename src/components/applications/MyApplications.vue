<template>
  <div class="container py-5 px-0">
    <div class="text-center">
      <h2 class="mb-5">Applications</h2>
    </div>
    <div class="row gx-0 gx-sm-3 gx-lg-5 gx-xl-7">
      <MyApplicationItem
          v-for="application in applications"
          :application="application"
          :key="application.id"
      />
    </div>
  </div>
</template>

<script>
import MyApplicationItem from "@/components/applications/MyApplicationItem";

export default {
  name: "my-applications",
  components: {MyApplicationItem},
  props: {
    applications: {
      type: Array,
      required: true,
    }
  }
}
</script>

<style lang="scss">
.applications {
  background: #F5F5F5;
}
</style>