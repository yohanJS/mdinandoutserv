<template>
  <div class="container split-bg pt-5 pb-5">
    <div class="row d-flex justify-content-center">
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
      <div class="row d-flex justify-content-center">
        <form
          class="col-12 col-md-6 mt-5 border border-1 shadow-lg rounded-5 p-3 bg-white"
          id="reviewForm"
          v-on:submit.prevent="sendEmailForm"
        >
          <div class="col-12 col-md-6 m-auto mt-3">
            <label class="form-label fw-bold">Full Name</label>
            <input
              required
              class="form-control"
              for="author"
              aria-label="Enter author's name"
              v-model="name"
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
              for="email"
              aria-label="Enter email"
              v-model="email"
              type="tel"
            />
          </div>
          <!-- <div class="col-12 col-md-6 m-auto mt-3">
            <label class="form-label fw-bold">Zip Code</label>
            <input
              required
              class="form-control"
              for="zipCode"
              aria-label="Enter zip code"
              v-model="zipCode"
              type="tel"
            />
          </div> -->
          <div class="col-12 col-md-6 m-auto mt-3">
            <label class="form-label fw-bold">Special Notes</label>
            <textarea
              required
              class="form-control"
              for="notes"
              aria-label="Enter notes"
              v-model="notes"
              rows="4"
              cols="50"
            >
            </textarea>
          </div>

          <div class="col-12 text-center">
            <button
              type="submit"
              id="submit"
              class="btn btn-lg rounded-pill btn-color btn-text-color fw-bold mt-5 mb-4"
              style="width: 250px"
            >
              Submit
            </button>
          </div>
        </form>
        <div v-if="successMessage" class="alert alert-success mt-2" role="alert">
          {{ successMessage }}
        </div>
        <div v-if="errorMessage" class="alert alert-danger" role="alert">
          {{ errorMessage }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      name: "",
      phoneNumber: "",
      email: "",
      notes: "",
      fromEmail: "yohangarcia@yohangarcia.com",
      toEmail: "yoanvaldes01@icloud.com",
      // toEmail: "alvaldes86@hotmail.com",
      subject: "Free Quote Requested",
      successMessage: "",
      errorMessage: "",
    };
  },
  methods: {
    async sendEmailForm() {
      try {
        const response = await axios
          .post(
            "/.netlify/functions/emails/sendRequest",
            {
              from: this.fromEmail,
              to: this.toEmail,
              subject: this.subject,
              parameters: {
                name: this.name,
                phoneNumber: this.phoneNumber,
                email: this.email,
                notes: this.notes,
              },
            },
            {
              headers: {
                "netlify-emails-secret": import.meta.env
                  .VITE_NETLIFY_EMAILS_SECRET,
              },
            }
          )
          .then(
            (this.name = ""),
            (this.phoneNumber = ""),
            (this.email = ""),
            (this.notes = ""),
            (this.successMessage = "We have received your request and will get back to you as soon as possible."),
          );
      } catch (error) {
        this.errorMessage = "Failed to submit form. Please try again.";
        console.error(response.data.message);
      }
    },
  },
};
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
  background-color: #cfdd51;
}
.btn-text-color {
  color: #1c434d;
}
.glass-button {
  background-color: rgba(
    255,
    255,
    255,
    0.1
  ); /* Adjust the opacity (0.3) as needed */
  backdrop-filter: blur(10px); /* Adjust the blur value as needed */
}
.btn-border-color {
  border: 1px solid #cfdd51;
}
.text-color {
  color: #cfdd51;
}
</style>
