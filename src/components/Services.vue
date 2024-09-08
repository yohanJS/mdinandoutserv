<template>
  <div id="services" class="container split-bg pt-5 pb-5" v-if="isMobile">
    <div class="col-12 text-center">
      <p class="text-uppercase pb-3">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 1 100 3" width="20" height="5">
          <rect width="100" height="3" fill="#cfdd51" />
        </svg>
        <strong class="text-white"> OUR SERVICES </strong>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 10 100 3" width="20" height="5">
          <rect width="100" height="6" fill="#cfdd51" />
        </svg>
      </p>
    </div>
    <div class="col-12 text-center">
      <h1 class="text-white display-1">A diverse range of services</h1>
    </div>
    <div class="col-12 mt-5">
      <div class="col-12 text-center">
        <button type="button" class="btn btn-lg rounded-pill glass-button btn-border-color text-white fw-bold mt-3"
          data-bs-toggle="modal" style="width: 250px;" data-bs-target="#staticAllServicesModalTarget">Browse all
          services
        </button>
      </div>
      <!-- All Services Modal -->
      <div class="modal fade" style="z-index: 99999;" id="staticAllServicesModalTarget" data-bs-backdrop="static"
        data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticAllServicesModal" aria-hidden="true">
        <div class="modal-dialog modal-fullscreen modal-dialog-scrollable">
          <div class="modal-content bg-color text-white">
            <div class="modal-header border-0 p-1">
              <CloseModalBtn></CloseModalBtn>
            </div>
            <div class="modal-body mt-3">
              <AllServices />
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
  <div class="container pt-5 mb-5 bg-color" v-else>
    <div class="col-12 text-center">
      <p class="text-uppercase pb-3">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 1 100 3" width="20" height="5">
          <rect width="100" height="3" fill="#cfdd51" />
        </svg>
        <strong class="text-white"> OUR SERVICES </strong>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 10 100 3" width="20" height="5">
          <rect width="100" height="6" fill="#cfdd51" />
        </svg>
      </p>
    </div>
    <div class="col-12 text-center">
      <h1 class="text-white display-1">A diverse range of services</h1>
    </div>
    <!--CARDS-->
    <!--ROW 1-->
    <div class="row split-bg pt-5 pb-5">
      <div class="col-12 col-md-4 text-center text-dark mt-5">
        <img src="../assets/card-1.png" class="img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Aluminum Pergola
        </h3>
        <p class="text-start m-3">
          Elevate your outdoor space with a sophisticated Aluminum Pergola that provides the perfect setting for
          cherished family moments and relaxation.
        </p>
      </div>
      <div class="col-12 col-md-4 text-center text-dark mt-5">
        <img src="../assets/card-2.png" class="img-fluid img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Outdoor Kitchen
        </h3>
        <p class="text-start m-3">
          We provide everything needed to prepare and serve your favorite meals outdoors, including ovens,
          refrigerators, and top-notch barbecues.
        </p>
      </div>
      <div class="col-12 col-md-4 text-center text-dark mt-5">
        <img src="../assets/card-3.png" class="img-fluid img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Patio Screen Enclosure
        </h3>
        <p class="text-start m-3">
          This is more than just a home improvement project; it enhances your lifestyle. Your new patio screen enclosure
          will become the focal point for family events.
        </p>
      </div>
    </div>
    <!--ROW 2-->
    <div class="row split-bg pt-5 pb-5">
      <div class="col-12 col-md-4 text-center text-dark mt-5">
        <img src="../assets/card-4.png" class="img-fluid img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Screen Repair
        </h3>
        <p class="text-start m-3">
          Our knowledgeable team can repair, replace, re-screen, and even craft custom screens and framing to suit your
          specific needs.
        </p>
      </div>
      <div class="col-12 col-md-4 text-center text-dark mt-5">
        <img src="../assets/card-5.png" class="img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Motorize Screen
        </h3>
        <p class="text-start m-3">
          For protection against UV rays, pests, weather, and other elements, motorized retractable screens are the
          ideal solution. Enjoy the outdoors in comfort.
        </p>
      </div>
      <div class="col-12 col-md-4 text-center text-dark mt-5">
        <img src="../assets/card-6.png" class="img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Outdoor Tv Installation
        </h3>
        <p class="text-start m-3">
          Patios and terraces are areas that are frequently forgotten.Transform your backyard into an outdoor
          entertainment space to maximize its potential.
        </p>
      </div>
    </div>
    <!--ROW 3-->
    <div class="row split-bg pt-5 pb-5">
      <div class="col-12 col-md-4 text-center text-dark mt-5">
        <img src="../assets/card-7.png" class="img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Fence
        </h3>
        <p class="text-start m-3">
          Enhance the appearance and individuality of your home with a stylish fence, as your exterior is the first
          impression visitors will have of your home.
        </p>
      </div>
      <div class="col-12 col-md-4 text-center text-dark mt-5">
        <img src="../assets/card-8.png" class="img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Composite Deck
        </h3>
        <p class="text-start m-3">
          Upgrade your outdoor area for dining, hosting guests, or simply unwinding under the sun. We are excited to
          make your Composite Deck vision a reality.
        </p>
      </div>
      <div class="col-12 col-md-4 text-center text-dark mt-5">
        <img src="../assets/card-9.png" class="img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Permit
        </h3>
        <p class="text-start m-3">
          Facilitates procedures for new construction and legalization.
        </p>
      </div>
    </div>
    <!--ROW 4-->
    <div class="row split-bg pt-5 pb-5">
      <div class="col-12 col-md-4 text-center text-dark mt-5">
        <img src="../assets/card-10.png" class="img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Aluminum Patio Cover
        </h3>
        <p class="text-start m-3">
          We offer patio cover designs to fit your lifestyle and needs. Enjoy your outdoor living space all year round,
          no matter the weather.
        </p>
      </div>
      <div class="col-12 col-md-4 text-center text-dark mt-5">
        <img src="../assets/card-11.png" class="img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Terrace
        </h3>
        <p class="text-start m-3">
          MD IN & OUT SERVICES is committed to designing beautiful, modern terraces that match your lifestyle. Create a
          gorgeous and functional outdoor living space.
        </p>
      </div>
      <div class="col-12 col-md-4 text-center text-dark mt-5">
        <img src="../assets/card-12.png" class="img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">3D RENDERS
        </h3>
        <p class="text-start m-3">
          3D RENDERS allow you to bring your dream spaces before it is built. We know we can make your project
          successful.
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
import AllServices from './AllServices.vue'
import CloseModalBtn from './CloseModalBtn.vue'
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
