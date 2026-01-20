<script setup>
import PortfolioContent from './components/PortfolioContent.vue'
import ContactForm from './components/ContactForm.vue'
</script>

<template>
  <div class="min-h-full">
    <div class="home-bg-animation"></div>
    <section class="home-hero">
      <img alt="Nurul Azim avatar" class="avatar" src="./assets/logo.svg" width="140" height="140" />
      <h1 class="hero-title">Nurul Azim</h1>
      <h2 class="hero-role">Senior Fullstack Developer</h2>
      <div class="hero-links">
        <a href="tel:01843701272" class="icon-btn" title="Call"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M15 12a3 3 0 0 1-6 0"/></svg></a>
        <a href="mailto:azimnurul1993@gmail.com" class="icon-btn" title="Email"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="7" width="18" height="10" rx="2"/><polyline points="3 7 12 13 21 7"/></svg></a>
        <a href="https://github.com/Azim1993" target="_blank" class="icon-btn" title="GitHub"><svg width="24" height="24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M9 9c0-1.1.9-2 2-2s2 .9 2 2"/><path d="M9 15c0-1.1.9-2 2-2s2 .9 2 2"/></svg></a>
      </div>
    </section>
  </div>

  <div class="content-wrapper">
    <portfolio-content />
    <contact-form />
  </div>
</template>

<style scoped>
body {
  background: #181c24;
  font-family: 'Inter', 'Segoe UI', Arial, sans-serif;
}
.home-bg-animation {
  position: fixed;
  top: 0; left: 0; right: 0; bottom: 0;
  width: 100vw;
  height: 100vh;
  z-index: -1;
  background: linear-gradient(270deg, #42b983, #2c3e50, #181c24, #42b983);
  background-size: 800% 800%;
  animation: gradientMove 18s ease-in-out infinite;
}
@keyframes gradientMove {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}
.home-hero {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: #fff;
  background: transparent;
  padding: 3rem 1rem 2rem 1rem;
}
.avatar {
  border-radius: 50%;
  border: 4px solid #fff;
  box-shadow: 0 4px 24px rgba(44,62,80,0.12);
  width: 140px;
  height: 140px;
  margin-bottom: 1.2rem;
}
.hero-title {
  font-size: 2.7rem;
  font-weight: 700;
  margin-bottom: 0.3rem;
  letter-spacing: 1px;
}
.hero-role {
  font-size: 1.3rem;
  font-weight: 500;
  color: #b2f5ea;
  margin-bottom: 1.2rem;
}
.hero-links {
  display: flex;
  gap: 1.2rem;
  justify-content: center;
  margin-top: 1.2rem;
}
.icon-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 44px;
  height: 44px;
  background: #fff;
  color: #42b983;
  border-radius: 50%;
  box-shadow: 0 2px 8px rgba(44,62,80,0.10);
  transition: background 0.2s, color 0.2s;
  text-decoration: none;
  font-size: 1.2rem;
}
.icon-btn:hover {
  background: #42b983;
  color: #fff;
}
.content-wrapper {
  position: relative;
  z-index: 1;
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem 1rem 3rem 1rem;
}
@media (max-width: 600px) {
  .home-hero {
    padding: 2rem 1rem;
  }
  .hero-title {
    font-size: 2rem;
  }
  .avatar {
    width: 100px;
    height: 100px;
  }
  .content-wrapper {
    padding: 1rem 0.5rem 2rem 0.5rem;
  }
}
</style>
