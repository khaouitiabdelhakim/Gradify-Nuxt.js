<!-- pages/index.vue -->
<template>
    <div class="gradient-container">
        <GradientCard v-for="(gradient, index) in gradients" :key="index" :gradient="gradient" />
    </div>
</template>

<script setup>
import GradientCard from '~/components/GradientCard.vue';
import gradients from '~/assets/gradients.js';
</script>

<style scoped>
.gradient-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 20px;
}
</style>