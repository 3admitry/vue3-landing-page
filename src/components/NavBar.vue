<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light py-3 bg-white shadow">
    <div class="container">
      <a class="navbar-brand" href="#">
        <img src="@/assets/images/logo.svg" alt="Success Craft" class="header__logo__img">
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
              data-bs-target="#navbarSupportedContent"
              aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Переключатель навигации">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0 text-uppercase fs-5 gap-3">
          <li class="nav-item">
            <a class="nav-link active" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="/#about-us">About us</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="/#frameworks">Frameworks</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="/#applications">Applications</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="/#contact-us">Contact us</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavBar"
}
</script>

<style scoped lang="scss">
.header {
  .header__logo__img {
    max-height: 40px;
  }
}
</style>