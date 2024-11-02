<template>
    <div class="gradient-card-container">
      <!-- Main Gradient Card -->
      <div class="gradient-card" :style="gradientStyle">
      </div>
  
      <!-- Color Swatches Underneath -->
      <div class="color-swatches">
        <div
          v-for="(color, index) in [gradient.start, gradient.end]"
          :key="index"
          :style="{ backgroundColor: color }"
          class="color-swatch"
          @click="copyToClipboard(color)"
        >
          <span class="color-text">{{ color }}</span>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { computed, ref } from 'vue';
  
  const props = defineProps({
    gradient: {
      type: Object,
      required: true,
    },
  });
  
  const gradientStyle = computed(() => ({
    background: `linear-gradient(135deg, ${props.gradient.start}, ${props.gradient.end})`,
  }));
  
  // Clipboard Copy Function
  function copyToClipboard(color) {
    navigator.clipboard.writeText(color).then(() => {
      alert(`Copied: ${color}`);
    });
  }
  </script>
  
  <style scoped>
  .gradient-card-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 10px;
    margin-bottom: 30px;
  }
  
  .gradient-card {
    width: 300px;
    height: 160px;
    border-radius: 10px;
    display: flex;
    align-items: flex-end;
    justify-content: center;
    color: white;
    font-weight: bold;
    padding-bottom: 10px;
    text-align: center;
    margin-bottom: 10px;
  }
  
  .color-swatches {
    display: flex;
    gap: 10px;
  }
  
  .color-swatch {
    width: 80px;
    height: 40px;
    border-radius: 5px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-weight: bold;
    cursor: pointer;
    position: relative;
    transition: transform 0.2s;
  }
  
  .color-swatch:hover {
    transform: scale(1.1);
  }
  
  .color-text {
    font-size: 0.9em;
    pointer-events: none;
  }
  </style>
  