<template>
  <div class="hero-section">
    <div class="hero-content">
      <h1>Onam Festival</h1>
      <h2>September 14 -September 17, 2024</h2>
    </div>
    <button class="learn-more-button">
      <span>Learn More</span>
    </button>
  </div>
</template>

<script>
export default {
  name: 'HeroSection'
}
</script>

<style scoped>
.hero-section {
  display: flex;
  min-height: 480px;
  flex-direction: column;
  gap: 1.5rem;
  background-image: linear-gradient(rgba(0, 0, 0, 0.1) 0%, rgba(0, 0, 0, 0.4) 100%), url("https://cdn.usegalileo.ai/sdxl10/1ffc7dbe-9c26-471b-ab13-0edcd7d80ec8.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  align-items: flex-start;
  justify-content: flex-end;
  padding: 1rem;
  padding-bottom: 2.5rem;
  border-radius: 0.75rem;
}
.hero-content {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  text-align: left;
}

.hero-content h1 {
  color: white;
  font-size: 3rem;
  font-weight: 900;
  line-height: 1.25;
  letter-spacing: -0.033em;
}

.hero-content h2 {
  color: white;
  font-size: 1rem;
  font-weight: 400;
  line-height: normal;
}

.learn-more-button {
  background-color: #f2a60d;
  color: #181611;
  display: flex;
  min-width: 84px;
  max-width: 480px;
  cursor: pointer;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  border-radius: 9999px;
  height: 2.5rem;
  padding: 0 1rem;
  font-size: 0.875rem;
  font-weight: 700;
  line-height: normal;
  letter-spacing: 0.015em;
}

.hero-section {
  transition: transform 0.3s ease;
}

.hero-section:hover {
  transform: scale(1.02);
}

.learn-more-button:hover {
  background-color: #e09600;
}
</style>
