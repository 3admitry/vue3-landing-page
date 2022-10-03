<template>
  <div class="container pt-5 pb-4">
    <div class="row text-center">
      <h2 class="mb-5">Frameworks</h2>
    </div>
    <MyFrameworksItem
        v-for="framework in frameworks"
        :framework="framework"
        :key="framework.id"
    />
  </div>
</template>

<script>
import MyFrameworksItem from "@/components/frameworks/MyFrameworksItem";

export default {
  name: "my-frameworks",
  components: {MyFrameworksItem},
  props: {
    frameworks: {
      type: Array,
      required: true,
    }
  }
}
</script>

<style lang="scss">
.frameworks {
  background: #F5F5F5;
}
</style>