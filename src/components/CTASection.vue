<template>
  <div class="cta-section">
    <h1>Experience Onam</h1>
      <button class="book-now-button">
        <span>Book Now</span>
      </button>
  </div>
</template>

<script>
export default {
  name: 'CTASection'
}
</script>

<style scoped>
  .cta-section {
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  gap: 1.5rem;
  padding: 2.5rem 1rem 5rem;
  text-align: center;
}

.cta-section h1 {
  color: #181611;
  font-size: 2.5rem;
  font-weight: 900;
  line-height: 1.25;
  letter-spacing: -0.033em;
  max-width: 720px;
  margin: 0 auto;
}

.book-now-button {
  background-color: #f2a60d;
  color: #181611;
  display: flex;
  min-width: 84px;
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
.book-now-button:hover {
  background-color: #e09600;
}
</style>
