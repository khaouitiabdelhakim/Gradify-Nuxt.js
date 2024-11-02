<!-- pages/index.vue -->
<template>
    <Header />
    <div class="gradient-container">
        <GradientCard v-for="(gradient, index) in gradients" :key="index" :gradient="gradient" />
    </div>
    <Footer />
</template>






<script setup>
import GradientCard from '~/components/GradientCard.vue';
import gradients from '~/assets/gradients.js';
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue';
</script>

<style scoped>
.gradient-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 20px;
}
</style>