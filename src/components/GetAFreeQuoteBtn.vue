<template>
    <div class="col-12 col-md-6 text-center mt-5">
      <button id="freeQuoteBtn" class="btn btn-lg rounded-pill btn-color btn-text-color fw-bold mb-2"
        style="width: 200px;" @click="openModal">Get a free quote</button>
  
      <!-- Bootstrap Modal -->
      <div class="modal fade" id="quoteModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog modal-dialog-centered" role="document">
          <div class="modal-content">
            <div class="modal-header">
              <h5 class="modal-title">Request a Quote</h5>
              <button type="button" class="btn-close" @click="closeModal"></button>
            </div>
            <div class="modal-body">
              <ContactForm />
            </div>
            <div class="modal-footer">
              <button type="button" class="btn btn-secondary" @click="closeModal">Close</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { onMounted } from 'vue';
  import { Modal } from 'bootstrap'; 
  import ContactForm from './ContactForm.vue';
  
  let modalInstance = null;
  
  const openModal = () => {
    modalInstance.show();
  };
  
  const closeModal = () => {
    modalInstance.hide();
  };
  
  onMounted(() => {
    const modalElement = document.getElementById('quoteModal');
    modalInstance = new Modal(modalElement);
  });
  </script>
  
  <style scoped>
  .modal-backdrop {
    background-color: rgba(0, 0, 0, 0.5);
  }
  
  .modal-dialog {
    max-width: 500px;
  }
  
  .btn-color {
    background-color: #CFDD51;
  }
  
  .btn-text-color {
    color: #1C434D;
  }
  </style>
  