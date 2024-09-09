<template>
  <div id="about" class="container section-bg">
    <div class="min-vh-100 row d-flex align-items-center">
      <div class="col-12 text-color">
        <p class="text-uppercase pb-1 m-0 text-center">
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 10 100 3" width="20" height="5">
            <rect width="100" height="6" fill="#cfdd51" />
          </svg>
          <strong class="text-color"> ABOUT US </strong>
          <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 10 100 3" width="20" height="5">
            <rect width="100" height="6" fill="#cfdd51" />
          </svg>
        </p>
        <p class="p-3">
          MD In & Out Services is a versatile company that provides a wide variety of services tailored to meet the
          unique
          needs of your home. Our mission is to help our clients bring their dream spaces to life,
          allowing them to transform their homes into something truly extraordinary.
        </p>
        <!-- Button trigger modal -->
        <div class="col-12 col-md-6 text-center" v-if="isMobile">
          <a type="button" class="text-muted text-decoration-none" data-bs-toggle="modal"
            data-bs-target="#staticBackdropModal">
            Read more
          </a>
        </div>
        <div class="p-3" v-else>
          <p> One of our family hobbies is spending time in our yard, creating beautiful memories within the
            comfort of our home.
            This is why we are committed to assisting every customer in personalizing their spaces, both
            indoors
            and outdoors,
            to suit their budget. Our goal is to provide a suitable and inviting atmosphere where families can
            enjoy quality time together.
          </p>
          <p>
            When my wife and I were searching for our dream home, one of our priorities was having a patio
            with a
            pergola where our children could play.
            Although  we found the ideal home, there was one thing missing in the backyard that would make
            family
            time more enjoyable: a roofed space. 
            It wasn't until we built a pergola that we starting enjoying our patio and home even more.
          </p>
          <p>
            Family gatherings no longer require a purposeful occasion. For us, every day is a celebration. All
            we
            need is some nice BBQ and good company.
            This is what we love about MD In & Out Services; our experience can be yours too.
          </p>
          <p>What are you looking for? Is it the same thing we once needed? Do not wait any longer.
          </p>
          <p>
            Come in and learn about all of our services; we're here to help!
          </p>
        </div>
        <!-- Modal -->
        <div class="modal fade" style="z-index: 99999;" id="staticBackdropModal" data-bs-backdrop="static"
          data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropModalLabel" aria-hidden="true">
          <div class="modal-dialog modal-fullscreen modal-dialog-scrollable">
            <div class="modal-content bg-color text-white">
              <div class="modal-header border-0 p-1">
                <CloseModalBtn></CloseModalBtn>
              </div>
              <div class="modal-body mt-3">
                <div class="col-12 text-color mb-5">
                  <p class="text-uppercase pb-1 m-0 text-center">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 10 100 3" width="20" height="5">
                      <rect width="100" height="6" fill="#cfdd51" />
                    </svg>
                    <strong class="text-white"> ABOUT US </strong>
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 10 100 3" width="20" height="5">
                      <rect width="100" height="6" fill="#cfdd51" />
                    </svg>
                  </p>
                </div>
                <p> One of our family hobbies is spending time in our yard, creating beautiful memories within the
                  comfort of our home.
                  This is why we are committed to assisting every customer in personalizing their spaces, both
                  indoors
                  and outdoors,
                  to suit their budget. Our goal is to provide a suitable and inviting atmosphere where families can
                  enjoy quality time together.
                </p>
                <p>
                  When my wife and I were searching for our dream home, one of our priorities was having a patio
                  with a
                  pergola where our children could play.
                  Although  we found the ideal home, there was one thing missing in the backyard that would make
                  family
                  time more enjoyable: a roofed space. 
                  It wasn't until we built a pergola that we starting enjoying our patio and home even more.
                </p>
                <p>
                  Family gatherings no longer require a purposeful occasion. For us, every day is a celebration. All
                  we
                  need is some nice BBQ and good company.
                  This is what we love about MD In & Out Services; our experience can be yours too.
                </p>
                <p>What are you looking for? Is it the same thing we once needed? Do not wait any longer.
                </p>
                <p>
                  Come in and learn about all of our services; we're here to help!
                </p>
                <div class="col-12 col-md-6 text-center mt-5">
                  <button id="freeQuoteBtn" class="btn btn-lg rounded-pill btn-color btn-text-color fw-bold mb-2"
                    style="width: 200px;" v-on:click=goToContactForm()>Get a free quote</button>
                  <button id="servicesBtn"
                    class="btn btn-lg rounded-pill glass-button btn-border-color text-white fw-bold"
                    style="width: 200px;" v-on:click=goToServices()>All services</button>
                </div>
                <Footer />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.w-10 {
  width: 10%;
}

.section-bg {
  background-color: #f5f5f5;
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
  background-color: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
}

.btn-border-color {
  border: 1px solid #CFDD51;
}

.text-color {
  color: #0A323D;
}
</style>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';
import { Modal } from 'bootstrap';
import Footer from './Footer.vue';
import CloseModalBtn from './CloseModalBtn.vue'

const isMobile = ref(false);

// Methods
const goToContactForm = () => {
  window.location.href = '#getQuoteSection';
  hideModal();
};

const goToServices = () => {
  window.location.href = '#services';
  hideModal();
};

const hideModal = () => {
  let staticBackdropModal = document.getElementById("staticBackdropModal");
  if (staticBackdropModal) {
    let modalInstance = Modal.getInstance(staticBackdropModal);
    if (modalInstance) {
      modalInstance.hide();
    }
  }
};

// Lifecycle hooks
onMounted(() => {
  isMobile.value = window.innerWidth <= 768;

  const handleResize = () => {
    isMobile.value = window.innerWidth <= 768;
  };

  window.addEventListener('resize', handleResize);

  // Clean up the event listener on unmount
  onBeforeUnmount(() => {
    window.removeEventListener('resize', handleResize);
  });
});

</script>