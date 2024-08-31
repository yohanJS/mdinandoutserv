<template>
  <div id="services" class="container split-bg pt-5 pb-5" v-if="isMobile">
    <div class="col-12 text-center">
      <p class="text-uppercase pb-3">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 1 100 3" width="20" height="5">
          <rect width="100" height="3" fill="#cfdd51" />
        </svg>
        <strong class="text-white"> OUR SERVICES</strong>
      </p>
    </div>
    <div class="col-12 text-center">
      <h1 class="text-white display-1">A diverse range of services</h1>
    </div>
    <div class="col-12 mt-5">
      <div class="col-12 text-center">
          <button type="button" class="btn btn-lg rounded-pill glass-button btn-border-color text-white fw-bold mt-3" data-bs-toggle="modal"
          style="width: 250px;" data-bs-target="#staticAllServicesModalTarget">Browse all services
        </button>
      </div>
      <!-- All Services Modal -->
        <!-- Modal -->
        <div class="modal fade" style="z-index: 99999;" id="staticAllServicesModalTarget" data-bs-backdrop="static"
          data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticAllServicesModal" aria-hidden="true">
          <div class="modal-dialog modal-fullscreen modal-dialog-scrollable">
            <div class="modal-content bg-color text-white">
              <div class="modal-header border-0">
                <button type="button" class="btn-close bg-light" data-bs-dismiss="modal" aria-label="Close"></button>
              </div>
              <div class="modal-body mt-3">
                <AllServices/>
                <Footer />
              </div>
            </div>
          </div>
        </div>
    </div>
    <div class="col-12 col-md-4 text-center mt-5">
      <img src="../assets/card-1.png" class="img-fluid border-bottom-right img-size shadow-lg" alt="...">
      <h3 class="text-start m-3">Aluminum Pergola
      </h3>
      <p class="text-start m-3">
        Create a space where you and your family can make lasting memories.
      </p>
    </div>
  </div>
  <div class="container" v-if="isMobile">
    <div class="row">
      <div class="col-12 col-md-4 text-center mt-5">
        <img src="../assets/card-2.png" class="img-fluid img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Outdoor Kitchen
        </h3>
        <p class="text-start m-3">
          Our outdoor kitchen specialists can help you plan and design your space.
        </p>
      </div>
      <div class="col-12 col-md-4 text-center mt-5">
        <img src="../assets/card-9.png" class="img-fluid img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Permit
        </h3>
        <p class="text-start m-3">
          Permit procedures for new constructions and legalizations.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import AllServices from './AllServices.vue'
import Footer from './Footer.vue'

const isMobile = ref(false);

onMounted(() => {
  isMobile.value = window.innerWidth <= 768;
});

window.addEventListener('resize', () => {
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
  color: #1C434D;
}

.glass-button {
  background-color: rgba(255, 255, 255, 0.1);
  /* Adjust the opacity (0.3) as needed */
  backdrop-filter: blur(10px);
  /* Adjust the blur value as needed */
}

.btn-border-color {
  border: 1px solid #CFDD51;
}

.text-color {
  color: #cfdd51;
}

.border-bottom-right {
  border-bottom-right-radius: 195px;
}

.img-size {
  width: 85%;
  height: 330px;
}

.arrow-margin {
  margin-left: 20px;
}
</style>
