<template>
    <div class="col-12 col-md-6 text-center mt-5">
        <button id="freeQuoteBtn" class="btn btn-lg rounded-pill btn-color btn-text-color fw-bold mb-2"
            style="width: 200px;" v-on:click=goToContactForm()>Get a free quote</button>
    </div>
</template>


<script setup>
// Methods
const goToContactForm = () => {
    window.location.href = '#getQuoteSection';
    hideModal();
};

</script>

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