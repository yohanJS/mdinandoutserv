<template>
  <div class="row justify-content-center bg-color pb-2 pt-2 m-0">
    <div class="col-12 p-0 text-center" v-if="isMobile">
      <p class="m-0 txt-color">Let's talk <a href="tel:+1xxxxxxxxxx">(xxx) xxx-xxxx</a></p>
      <p class="m-0"><a href="mailto:xx@domain.com">xx@domain.com</a></p>
    </div>
    <div class="col-12 p-0 text-center" v-else>
      <p class="m-0">Let's talk <a href="tel:+1xxxxxxxxxx">(xxx) xxx-xxxx</a><span id="bar" class="p-2">|</span><a href="mailto:xx@domain.com">xx@domain.com</a></p>
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
a {
  text-decoration: none;
  color: #1C434D;
}
.bg-color {
  background-color: #F3F3F3;
}
.txt-color {
  color: #1C434D;
}
#bar {
  display: inline-block;
}

@media only screen and (max-width: 768px) {
  #bar {
    display: none;
  }
}
</style>
