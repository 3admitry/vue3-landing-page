<template>
  <div class="container">
    <div class="row py-5 my-5">
      <div class="col-12 col-lg-6 col d-flex align-items-center pe-5">
        <div class="about-us__content">
          <h2 class="">About us</h2>
          <p class="my-4 text-muted">
            Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the
            industry's
            standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to
            make a type specimen book. It has survived not only five centuries, but also the leap into electronic
            typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset
          </p>
          <div class="about-us__btns d-flex gap-3">
            <button type="button" class="btn btn-primary">Read more</button>
            <button type="button" class="btn btn-outline-primary">Contact Us</button>
          </div>
        </div>
      </div>
      <div class="col-12 col-lg-6 col pt-5 pt-lg-0">
        <div class="about-us__video-container">
          <iframe src="https://www.youtube.com/embed/Upex8hM6wRs"
                  title="Top 5 Front End Frameworks 2021 | Best Frontend Frameworks 2021 | Web Development"
                  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen></iframe>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutUs"
}
</script>

<style lang="scss">
.about-us {
  background: url("@/assets/images/bg_aboutus.jpg") left no-repeat;

  &__video-container {
    display: flex;
    flex-direction: column;
    height: 330px;
    justify-content: center;
    border-radius: 5px;
    overflow: hidden;
    width: 100%;

    iframe {
      width: 100%;
      height: 100%;
    }
  }
}
</style>