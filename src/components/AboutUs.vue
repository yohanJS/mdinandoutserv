<script>

import Footer from './Footer.vue'
export default {
  components: {
    Footer
  }
}
</script>

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
        <!-- <p class="p-3">
        What are you looking for? Is it the same thing we once needed?
      </p>
      <p class="p-3">
        Do not wait any longer. 
        Come in and learn about all of our services; we're here to help!
      </p> -->
        <!-- Button trigger modal -->
         <div class="col-12 text-center">
          <a type="button" class="text-color text-decoration-none" data-bs-toggle="modal" data-bs-target="#staticBackdrop">
          Read more
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-info-circle" viewBox="0 0 16 16">
                  <path d="M8 15A7 7 0 1 1 8 1a7 7 0 0 1 0 14m0 1A8 8 0 1 0 8 0a8 8 0 0 0 0 16"/>
                  <path d="m8.93 6.588-2.29.287-.082.38.45.083c.294.07.352.176.288.469l-.738 3.468c-.194.897.105 1.319.808 1.319.545 0 1.178-.252 1.465-.598l.088-.416c-.2.176-.492.246-.686.246-.275 0-.375-.193-.304-.533zM9 4.5a1 1 0 1 1-2 0 1 1 0 0 1 2 0"/>
                </svg>
        </a>
         </div>
        <!-- Modal -->
        <div class="modal fade" style="z-index: 99999;" id="staticBackdrop" data-bs-backdrop="static"
          data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
          <div class="modal-dialog modal-fullscreen modal-dialog-scrollable">
            <div class="modal-content bg-color text-white">
              <div class="modal-header border-0">
                <h1 class="modal-title fs-5" id="staticBackdropLabel">About Us</h1>
                <button type="button" class="btn-close bg-light" data-bs-dismiss="modal" aria-label="Close"></button>
              </div>
              <div class="modal-body mt-3">
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
                  <button id="freeQuoteBtn" class="btn btn-lg rounded-pill btn-color btn-text-color fw-bold mb-2" style="width: 200px;" onclick="window.location.href='#getQuote'">Get a free quote</button>
                  <button id="servicesBtn" class="btn btn-lg rounded-pill glass-button btn-border-color text-white fw-bold" style="width: 200px;" onclick="window.location.href='#services'">All services</button>
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