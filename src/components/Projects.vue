<template>
  <div class="container split-bg p-5" v-if="isMobile">
    <div class="col-12 text-center">
      <p class="text-uppercase pb-3 line">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 1 100 3"
          width="20"
          height="5"
        >
          <rect width="100" height="3" fill="#cfdd51" />
        </svg>
        <strong class="text-white"> OUR PROJECTS</strong>
      </p>
    </div>
    <div class="col-12 text-center">
      <h1 class="text-white display-1">Take a look at our projects</h1>
    </div>
    <div class="col-12 col-md-4 text-center mt-5" v-if="isMobile">
      <div class="image-container">
        <img
          src="../assets/project-img-1.png"
          class="img-fluid shadow-lg"
          alt="..."
        />
        <div class="text-overlay">
          <li class="text-start text-white m-2">Aluminum Pergola</li>
        </div>
      </div>
    </div>
  </div>
  <div class="container pb-5" v-if="isMobile">
    <div class="row">
      <div class="col-12 col-md-4 text-center mt-5">
        <div class="image-container">
          <img
            src="../assets/project-img-2.png"
            class="img-fluid shadow-lg"
            alt="..."
          />
          <div class="text-overlay">
            <li class="text-start text-white m-2">Composite Deck</li>
          </div>
        </div>
      </div>
      <div class="col-12 col-md-4 text-center mt-5">
        <div class="image-container">
          <img
            src="../assets/project-img-2.png"
            class="img-fluid shadow-lg"
            alt="..."
          />
          <div class="text-overlay">
            <li class="text-start text-white m-2">XXXXXX XX XXXXXX</li>
          </div>
        </div>
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
  background: linear-gradient(to bottom, #0a323d 60%, #ffffff 40%);
}
.bg-color {
  background-color: #0a323d;
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
.image-container {
  position: relative;
  display: inline-block;
}
.image-container img {
  display: block;
  width: 100%;
}
.text-overlay {
  position: absolute;
  bottom: 10px;
  left: 50%;
  transform: translateX(-50%);
  text-align: center;
  width: 90%; /* Adjust width as needed */
}
.text-overlay::before {
  content: "";
  display: block;
  border-top: 1px solid #cfdd51;
  margin: 0 auto 5px;
  width: 100%; /* Adjust width as needed */
}
li::marker {
  color: #cfdd51;
}
</style>
