<template>
  <div class="container split-bg pt-5 pb-5">
    <div class="row justify-content-center">
      <div class="col-12 col-md-6 text-center">
        <p class="text-uppercase pb-3">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 1 100 3"
                width="20"
                height="5"
              >
                <rect width="100" height="3" fill="#cfdd51" />
              </svg>
              <strong class="text-color"> CONTACT US </strong>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 1 100 3"
                width="20"
                height="5"
              >
                <rect width="100" height="3" fill="#cfdd51" />
              </svg>
            </p>
            <h1 class="text-white">Ready to get a free quote?</h1>
      </div>
      <div class="col-12 col-md-6">
        <form
          class="mt-5 border border-1 shadow-lg rounded-5 p-3 bg-white"
          id="reviewForm"
          v-on:submit.prevent="createReview"
        >
          <div class="col-12 col-md-6 m-auto mt-3">
            <label class="form-label fw-bold">Full Name</label>
            <input
              required
              class="form-control"
              for="author"
              aria-label="Enter author's name"
              v-model="author"
            />
          </div>
          <div class="col-12 col-md-6 m-auto mt-3">
            <label class="form-label fw-bold">Phone</label>
            <input
              required
              class="form-control"
              for="phoneNumber"
              aria-label="Enter phone number"
              v-model="phoneNumber"
              type="tel"
            />
          </div>
          <div class="col-12 col-md-6 m-auto mt-3">
            <label class="form-label fw-bold">Email</label>
            <input
              required
              class="form-control"
              for="phoneNumber"
              aria-label="Enter phone number"
              v-model="phoneNumber"
              type="tel"
            />
          </div>
          <div class="col-12 col-md-6 m-auto mt-3">
            <label class="form-label fw-bold">Zip Code</label>
            <input
              required
              class="form-control"
              for="phoneNumber"
              aria-label="Enter phone number"
              v-model="phoneNumber"
              type="tel"
            />
          </div>

          <div class="col-12 text-center">
            <button type="submit" id="submit" class="btn btn-lg rounded-pill btn-color btn-text-color fw-bold mt-5 mb-4" style="width: 250px;">
              Submit
            </button>
          </div>
    </form>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";

const isMobile = ref(false);

onMounted(() => {
  isMobile.value = window.innerWidth <= 768;
});

window.addEventListener("resize", () => {
  isMobile.value = window.innerWidth <= 768;
});
</script>

<style scoped>
.split-bg {
  background: linear-gradient(to bottom, #0a323d 40%, #ffffff 40%);
}
.bg-color {
  background-color: #0a323d;
}
.bg-color {
    background-color: #0a323d;
  }
  .btn-color {
    background-color: #CFDD51;
  }
  .btn-text-color {
    color: #1C434D;
  }
  .glass-button {
    background-color: rgba(255, 255, 255, 0.1); /* Adjust the opacity (0.3) as needed */
    backdrop-filter: blur(10px); /* Adjust the blur value as needed */
  }
  .btn-border-color {
    border: 1px solid #CFDD51;
  }
  .text-color {
    color: #cfdd51;
  }
</style>
