<template>
    <div>
      <!-- Floating Booking Icon -->
      <a 
        id="Setmore_button_iframe"
        href="https://mdinoutservices.setmore.com"
        rel="noopener noreferrer"
        class="booking-icon"
        >
        <i class="bi bi-calendar-fill"></i>
        <span class="booking-text">Book Now</span>
      </a>
    </div>
  </template>
  
  <script>
  export default {
    name: "BookingButton",
    mounted() {
      // Inject Setmore script dynamically
      const script = document.createElement("script");
      script.id = "setmore_script";
      script.type = "text/javascript";
      script.src =
        "https://mdinoutservices.setmore.com";
      document.body.appendChild(script);
    },
  };
  </script>
  
  <style scoped>
  /* Styles for the floating booking button */
  .booking-icon {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background-color: #cfdd51; /* Primary color */
    color: #1C434D;
    border-radius: 30px; /* Oval appearance to fit text */
    height: 35px;
    padding: 0 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    z-index: 1000;
    transition: background-color 0.3s ease;
  }
  
  .booking-icon:hover {
    background-color: #b8c043; /* Darker version of primary color */
    text-decoration: none;
  }
  
  .booking-icon i {
    font-size: 1.5rem; /* Size of the calendar icon */
    margin-right: 10px;
  }
  
  .booking-text {
    font-size: 1rem; /* Adjust text size */
    font-weight: bold;
    color: #1C434D;
  }
  </style>
  