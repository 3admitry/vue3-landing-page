<template>
  <div class="container py-5">
    <div class="row text-center">
      <h2 class="mb-5">Contact Us</h2>
    </div>
    <form
        class="row needs-validation"
        id="app-form"
        @submit="checkForm"
        novalidate
    >
      <div class="col-6 col-md-6 col-xl-3 col mb-3">
        <label for="formGroupFirstName" class="form-label">First Name *</label>
        <input
            type="text"
            name="firstName"
            v-model="firstName"
            class="form-control"
            id="formGroupFirstName"
            placeholder="Enter your First Name"
            required
        >
        <div class="valid-feedback">It's Ok!</div>
        <div class="invalid-feedback">Please, type your First Name</div>
      </div>
      <div class="col-6 col-md-6 col-xl-3 col mb-3">
        <label for="formGroupLastName" class="form-label">Last Name *</label>
        <input
            type="text"
            name="lastName"
            v-model="lastName"
            class="form-control"
            id="formGroupLastName"
            placeholder="Enter your Last Name"
            required
        >
        <div class="valid-feedback">It's Ok!</div>
        <div class="invalid-feedback">Please, type your Last Name</div>
      </div>
      <div class="col-6 col-md-6 col-xl-3 col mb-3">
        <label for="formGroupCompany" class="form-label">Company *</label>
        <input
            type="text"
            name="company"
            v-model="company"
            class="form-control"
            id="formGroupCompany"
            placeholder="Enter Your Company"
            required
        >
        <div class="valid-feedback">It's Ok!</div>
        <div class="invalid-feedback">Please, type Your Company</div>
      </div>
      <div class="col-6 col-md-6 col-xl-3 col mb-3">
        <label for="formGroupEmail" class="form-label">Email *</label>
        <input
            type="email"
            name="email"
            v-model="email"
            class="form-control"
            id="formGroupEmail"
            placeholder="Enter Your Email"
            required
        >
        <div class="valid-feedback">It's Ok!</div>
        <div class="invalid-feedback">Please, type valid Email</div>
      </div>
      <div class="col-6 col-md-6 col-xl-3 col mb-3">
        <label for="formGroupJobTitle" class="form-label">Job Title *</label>
        <input
            type="text"
            name="jobTitle"
            v-model="jobTitle"
            class="form-control"
            id="formGroupJobTitle"
            placeholder="Enter Your Job Title"
            required
        >
        <div class="valid-feedback">It's Ok!</div>
        <div class="invalid-feedback">Please, type Your Job Title</div>
      </div>
      <div class="col-6 col-md-6 col-xl-3 col mb-3">
        <label for="formGroupCountry" class="form-label">Country *</label>
        <input
            type="text"
            name="country"
            v-model="country"
            class="form-control"
            id="formGroupCountry"
            placeholder="Enter Your Country"
            required
        >
        <div class="valid-feedback">It's Ok!</div>
        <div class="invalid-feedback">Please, type Your Country</div>
      </div>
      <div class="col-6 col-md-6 col-xl-3 col mb-3">
        <label for="formGroupState" class="form-label">State *</label>
        <input
            type="text"
            name="state"
            v-model="state"
            class="form-control"
            id="formGroupState"
            placeholder="Enter Your State"
            required
        >
        <div class="valid-feedback">It's Ok!</div>
        <div class="invalid-feedback">Please, type Your State</div>
      </div>
      <div class="col-6 col-md-6 col-xl-3 col mb-3">
        <label for="formGroupZipCode" class="form-label">Zip code *</label>
        <input
            type="number"
            name="zipCode"
            v-model.number="zipCode"
            class="form-control"
            id="formGroupZipCode"
            placeholder="Enter Your Zip code"
            required
        >
        <div class="valid-feedback">It's Ok!</div>
        <div class="invalid-feedback">Please, type correct Zip code</div>
      </div>

      <div class="d-flex justify-content-center py-3">
        <button type="submit" class="btn btn-primary">Submit</button>
      </div>
    </form>
  </div>
  <MyModal v-model:show="isDialogOpen"/>
</template>

<script>
import MyModal from "@/components/UI/MyModal";

export default {
  name: "ContactUs",
  components: {MyModal},

  data() {
    return {
      firstName: '',
      lastName: '',
      company: '',
      email: '',
      jobTitle: '',
      country: '',
      state: '',
      zipCode: '',
      isDialogOpen: false,
    }
  },
  watch: {
    isDialogOpen(newVal) {
      if (newVal) {
        setTimeout(() => {
          this.isDialogOpen = false;
        }, 3000)
      }
    }
  },
  methods: {
    showModal() {
      this.isDialogOpen = true;
    },
    checkForm: function (e) {
      if (e.target.checkValidity()) {
        this.showModal();
      }
      e.target.classList.add('was-validated');
      e.preventDefault();
    },
  }
}
</script>

<style lang="scss">
.form-control {
  background-color: #f8f8f8;
  border: none;
}
</style>