<template>
    <footer class="app-footer">
        <!-- Logo and Description -->
        <div class="footer-logo">
            <img :src="logo" alt="Gradify Logo" class="logo" />
            <p class="description">Gradify makes exploring and copying beautiful gradients a breeze.</p>
        </div>

        <!-- Copyright Information -->
        <p class="copyright">
            © KHAOUITI Apps 2024 - {{ currentYear }}
        </p>

        <!-- Social Media Links -->
        <div class="social-links">
            <a href="https://github.com/khaouitiabdelhakim" target="_blank" aria-label="GitHub">
                <font-awesome-icon icon="fa-brands fa-github" class="icon" />
            </a>
            <a href="https://www.linkedin.com/in/khaouitiabdelhakim/" target="_blank" aria-label="LinkedIn">
                <font-awesome-icon icon="fa-brands fa-linkedin" class="icon" />
            </a>
        </div>
    </footer>
</template>

<script setup>
import logo from '~/assets/logo.png'
const currentYear = new Date().getFullYear()
</script>

<style scoped>
.app-footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: 20px;
    color: #fff;
}

.footer-logo {
    display: flex;
    align-items: center;
    flex-direction: column;
    margin-bottom: 10px;
}

.logo {
    width: 80px;
    height: auto;
    margin-bottom: 10px;
}

.description {
    font-size: 0.9em;
    color: #4e4e4e;
    max-width: 300px;
}

.copyright {
    font-size: 0.8em;
    color: #474747;
    margin: 5px 0;
}

.social-links {
    display: flex;
    gap: 15px;
    margin-top: 10px;
}

.icon {
    font-size: 1.5em;
    color: #fff;
    transition: color 0.3s;
}

.icon:hover {
    color: #1da1f2;
    /* Change this to your preferred color */
}
</style>