  <template>
    <div class="container-fluid p-0 bg-color">
      <div class="row g-0">
        <div class="col-md-12 shadow-lg position-relative">

          <!-- <video autoplay loop muted playsinline>
            <source src="../assets/web _md_in and out services.mp4" type="video/mp4">
          </video> -->
          <img src="../assets/bg-forNow.jpg" alt="Background Image" class="img-fluid" style="object-fit: cover; width: 100%; height: 100vh;">

          <div class="row d-flex flex-column pt-5 align-items-center text-center text-white" style="position: absolute; top: 0; left: 0; width: 100%; height: 100vh; z-index: 1;">
            <div id="section" class="col-12 mt-5">
              <p id="welcomeMsg" class="mt-4 text-uppercase pb-3">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 1 100 3"
                width="20"
                height="5"
              >
                <rect width="100" height="3" fill="#cfdd51" />
              </svg>
              Welcome to MD <strong class="text-color">IN & OUT</strong>
              SERVICES
            </p>        
            </div>
            <div class="col-12">
              <h1 class="display-1 fw-bold">MAKING YOUR DREAM HOME TRUE</h1>
            </div>
            <div class="row">
              <div class="col-12 mt-5">
                <button id="freeQuoteBtn" class="btn btn-lg rounded-pill btn-color btn-text-color fw-bold mr-r" style="width: 250px;" onclick="window.location.href='#getQuote'">Get a free quote</button>
                <button id="servicesBtn" class="btn btn-lg rounded-pill glass-button btn-border-color text-white fw-bold" style="width: 250px;" onclick="window.location.href='#services'">Browse all services</button>
              </div>
            </div>
           </div>
        </div>
      </div>
    </div>
  </template>

  <style scoped>
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
  .mr-r {
    margin-right: 20px;
  }
  </style>

<script setup>
import { ref, onMounted } from 'vue';

const isMobile = ref(false);
const isDesktop = ref(false);

onMounted(() => {
  isMobile.value = window.innerWidth < 600;
});

window.addEventListener('resize', () => {
  isMobile.value = window.innerWidth < 600;
  let freeQuoteBtn = document.getElementById("freeQuoteBtn");
  let servicesBtn = document.getElementById("servicesBtn");
  let welcomeMsg = document.getElementById("welcomeMsg");

  if (isMobile.value) {
    welcomeMsg.classList.remove("mt-4");
    freeQuoteBtn.classList.remove("mr-r");
    freeQuoteBtn.classList.add("mt-3");
    servicesBtn.classList.add("mt-3");
  } else {
    welcomeMsg.classList.add("mt-4");
    freeQuoteBtn.classList.add("mr-r");
  }
});
</script>
