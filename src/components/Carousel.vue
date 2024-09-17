<template>
  <div class="container">
    <div class="row">
      <div class="col-12 col-md-6 col-lg-4" v-for="(carousel, index) in carousels" :key="index">
        <div class="carousel-container my-4">
          <div class="carousel" :style="{ transform: `translateX(-${carousel.currentSlide * 100}%)` }">
            <div class="carousel-slide" v-for="(slide, slideIndex) in carousel.slides" :key="slideIndex">
              <div class="image-container">
                <img :src="slide.path" alt="Slide image" class="slide-path" />
              </div>
              <div class="text">{{ slide.text }}</div>
            </div>
          </div>
          <div class="carousel-controls">
            <button @click="prevSlide(index)">❮</button>
            <button @click="nextSlide(index)">❯</button>
          </div>
          <div class="carousel-indicators">
            <span v-for="(slide, slideIndex) in carousel.slides" :key="slideIndex"
              :class="{ active: carousel.currentSlide === slideIndex }" @click="goToSlide(index, slideIndex)"></span>
          </div>
        </div>
        <div class="">
          <LetsTalk :textColor="'#ffab00'" />
          <GetAFreeQuoteBtn />
        </div>
      </div>
    </div>
  </div>
</template>




<script>
import { ref } from 'vue';
import LetsTalk from './LetsTalk.vue';
import GetAFreeQuoteBtn from './GetAFreeQuoteBtn.vue';

export default {
  components: {
    LetsTalk,
    GetAFreeQuoteBtn
  },
  setup() {
    const carousels = ref([
      {
        currentSlide: 0,
        slides: [
          { path: new URL('../assets/prj-1.png', import.meta.url).href },
          { path: new URL('../assets/prj-2.png', import.meta.url).href },
        ]
      },
      {
        currentSlide: 0,
        slides: [
          { path: new URL('../assets/prj-3.png', import.meta.url).href },
          { path: new URL('../assets/prj-4.png', import.meta.url).href },
          { path: new URL('../assets/prj-5.png', import.meta.url).href },
        ]
      },
      // Add more carousels here as needed
    ]);

    const nextSlide = (carouselIndex) => {
      const carousel = carousels.value[carouselIndex];
      carousel.currentSlide = (carousel.currentSlide + 1) % carousel.slides.length;
    };

    const prevSlide = (carouselIndex) => {
      const carousel = carousels.value[carouselIndex];
      carousel.currentSlide = (carousel.currentSlide - 1 + carousel.slides.length) % carousel.slides.length;
    };

    const goToSlide = (carouselIndex, slideIndex) => {
      carousels.value[carouselIndex].currentSlide = slideIndex;
    };

    return {
      carousels,
      nextSlide,
      prevSlide,
      goToSlide
    };
  }
};
</script>




<style scoped>
.carousel-container {
  position: relative;
  width: 100%;
  max-width: 600px;
  margin: auto;
  overflow: hidden;
  background-color: #0a323d;
  color: white;
  border-radius: 8px;
  box-shadow: 5px 5px 8px 5px rgba(0, 0, 0, 0.1);
}

.carousel {
  display: flex;
  transition: transform 0.5s ease-in-out;
}

.carousel-slide {
  min-width: 100%;
  box-sizing: border-box;
  padding: 15px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.carousel-controls {
  display: flex;
  justify-content: space-between;
}

.carousel-controls button {
  background: none;
  border: none;
  color: white;
  font-size: 24px;
  cursor: pointer;
}

.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
}

.carousel-indicators span {
  width: 10px;
  height: 10px;
  background-color: white;
  border-radius: 50%;
  margin: 0 5px;
  cursor: pointer;
}

.carousel-indicators .active {
  background-color: #ffab00;
}

@media (min-width: 992px) {
  .carousel-container {
    max-width: 100%;
  }
}
</style>