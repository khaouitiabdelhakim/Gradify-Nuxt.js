<template>
    <header class="app-header">
        <img :src="logo" alt="Gradify Logo" class="logo" />
        <h1 class="app-title">Gradify</h1>
        <p class="slogan">Your Color Palette, Simplified.</p>
    </header>
</template>

<script setup>
import logo from '~/assets/logo.png';
</script>

<style scoped>
.app-header {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: 20px;
}

.logo {
    width: 200px;
    height: auto;
    margin-bottom: 4px;
}

.app-title {
    font-size: 1em;
    font-weight: bold;
    margin: 3px 0;
    font-family: 'Playwrite DE Grund', sans-serif;
}

.slogan {
    font-size: 1.2em;
    color: #888;
    font-family: 'Itim', cursive;
}
</style>
