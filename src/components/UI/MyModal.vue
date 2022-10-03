<template>
  <div class="dialog" v-if="show" @click="hideDialog">
    <div @click.stop class="dialog__content rounded bg-white px-4 py-3 m-auto align-items-center">
      <div class="text-center m-0 py-5">
        <h3>Thank you for getting in touch!</h3>
        <p class="text-muted">
          We appreciate you contacting Success Craft. One of our colleagues will get back in touch with you soon!Have a
          great day!
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MyModal",
  methods: {
    hideDialog() {
      this.$emit('update:show', false)
    }
  },
  props: {
    show: {
      type: Boolean,
      default: false,
    }
  }
}
</script>

<style scoped>
.dialog {
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
  background: rgb(0, 0, 0, 0.5);
  position: fixed;
  display: flex;
}

.dialog__content {
  min-height: 50px;
  width: 550px;
}
</style>