<template>
  <div class="container">
    <div class="row">
      <div class="col-12 col-lg-6 col">
        <div class="row">
          <div class="col"
               :style="{ background: 'url(' + require(`@/assets/images/meeting.jpg`) + ') center / cover' }"
          ></div>
          <div class="col py-4 ps-4">
            <h3>Setup a Meeting</h3>
            <div class="text-muted">
              Fill out our contact form and have someone get back to you within 24 hours.
            </div>
            <div class="pt-4">
              <button type="button" class="btn btn-primary">Schedule a Meeting</button>
            </div>
          </div>
        </div>
      </div>
      <div class="col-12 col-lg-6 col">
        <div class="row">
          <div class="col"
               :style="{ background: 'url(' + require(`@/assets/images/question.jpg`) + ') center / cover' }"
          ></div>
          <div class="col py-4 ps-4">
            <h3>Ask a Question.</h3>
            <div class="text-muted">
              Have a question? Just fill out our contact us form and we will get back to you.
            </div>
            <div class="pt-4">
              <button type="button" class="btn btn-primary">Ask a Question</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MeetsQuestions"
}
</script>

<style scoped>
</style>