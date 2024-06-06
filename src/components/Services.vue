  <template>
    <div class="container split-bg pt-5 pb-5" v-if="isMobile">
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
              <strong class="text-white"> OUR SERVICES</strong>
            </p>
      </div>
      <div class="col-12 text-center">
        <h1 class="text-white">A diverse range of services</h1>
      </div>
      <div class="col-12 text-center mt-5">
        <button class="btn btn-lg rounded-pill glass-button btn-border-color text-white fw-bold mt-3" style="width: 250px;">Browse all services</button>
      </div>
      <div class="col-12 col-md-4 text-center mt-5">
        <img src="../assets/card-1.png" class="img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Aluminum Pergola
          <span class="arrow-margin"><svg width="19" height="30" viewBox="0 0 19 28" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M3.94834 19.676L15.599 4.90053" stroke="#CFDD51" stroke-width="2" stroke-linecap="square"/>
          <path d="M15.9896 18.8074L15.9896 4.48787L4.63706 4.48787" stroke="#CFDD51" stroke-width="2" stroke-linecap="square"/>
          </svg>
          </span>
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
          <span class="arrow-margin"><svg width="19" height="30" viewBox="0 0 19 28" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M3.94834 19.676L15.599 4.90053" stroke="#CFDD51" stroke-width="2" stroke-linecap="square"/>
          <path d="M15.9896 18.8074L15.9896 4.48787L4.63706 4.48787" stroke="#CFDD51" stroke-width="2" stroke-linecap="square"/>
          </svg>
          </span>
        </h3>
        <p class="text-start m-3">
          Our outdoor kitchen specialists can help you plan and design your space.
        </p>
      </div>
      <div class="col-12 col-md-4 text-center mt-5">
        <img src="../assets/card-3.png" class="img-fluid img-fluid border-bottom-right img-size shadow-lg" alt="...">
        <h3 class="text-start m-3">Permit
          <span class="arrow-margin"><svg width="19" height="30" viewBox="0 0 19 28" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M3.94834 19.676L15.599 4.90053" stroke="#CFDD51" stroke-width="2" stroke-linecap="square"/>
          <path d="M15.9896 18.8074L15.9896 4.48787L4.63706 4.48787" stroke="#CFDD51" stroke-width="2" stroke-linecap="square"/>
          </svg>
          </span>
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
    background-color: rgba(255, 255, 255, 0.1); /* Adjust the opacity (0.3) as needed */
    backdrop-filter: blur(10px); /* Adjust the blur value as needed */
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
  
