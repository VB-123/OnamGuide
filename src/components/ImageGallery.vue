<script setup>
import { ref } from 'vue';

const carousel1 = new URL('@/assets/carousel1.jpeg', import.meta.url).href;
const carousel2 = new URL('@/assets/carousel2.jpeg', import.meta.url).href;
const carousel3 = new URL('@/assets/carousel3.jpeg', import.meta.url).href;
const carousel4 = new URL('@/assets/carousel4.jpeg', import.meta.url).href;

const currentIndex = ref(0);
const carouselItems = ref([
  {
    image: carousel1,
    title: 'The essence of Onam',
    description: 'Onam, is the festival, that lights up many households in Kerala.',
  },
  {
    image: carousel2,
    title: 'Onam touches each and every life in Kerala',
    description: 'From the poor to the rich, all people cherish and share the joy on this day.',
  },
  {
    image: carousel3,
    title: 'The winds on the shores, come alive!',
    description: 'The beauty of nature comes to life with the festivities in the city!',
  },
  {
    image: carousel4,
    title: 'It\'s Onam Time!',
    description: 'Brace yourselves, this festive season!',
  },
]);

const nextSlide = () => {
  currentIndex.value = (currentIndex.value + 1) % carouselItems.value.length;
};

const prevSlide = () => {
  currentIndex.value = (currentIndex.value - 1 + carouselItems.value.length) % carouselItems.value.length;
};
</script>

<template>
  <div class="carousel-container">
    <h2>Image Gallery</h2>
    <div class="carousel">
      <div class="carousel-inner" :style="{ transform: `translateX(-${currentIndex * 100}%)` }">
        <div v-for="(item, index) in carouselItems" :key="index" class="carousel-item">
          <img :src="item.image" :alt="item.title">
          <div class="carousel-caption">
            <h3>{{ item.title }}</h3>
            <p>{{ item.description }}</p>
          </div>
        </div>
      </div>
      <button class="carousel-control prev" @click="prevSlide">&lt;</button>
      <button class="carousel-control next" @click="nextSlide">&gt;</button>
    </div>
  </div>
</template>

<style scoped>
h2 {
  font-size: 2rem;
  font-weight: 700;
  line-height: 1.25;
  letter-spacing: -0.015em;
  margin-bottom: 1rem;
}

.carousel-container {
  max-width: 1000px;
  margin: 0 auto;
}

.carousel {
  position: relative;
  overflow: hidden;
  border-radius: 0.75rem;
}

.carousel-inner {
  display: flex;
  transition: transform 0.3s ease-in-out;
}

.carousel-item {
  flex: 0 0 100%;
  position: relative;
}

.carousel-item img {
  width: 100%;
  height: auto;
  object-fit: cover;
  aspect-ratio: 16/9;
  object-position: center;
  image-rendering: -webkit-optimize-contrast;
  image-rendering: crisp-edges;
}

.carousel-caption {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.45);
  color: white;
  padding: 1rem;
}

.carousel-caption h3 {
  margin: 0;
  font-size: 1.25rem;
}

.carousel-caption p {
  margin: 0.5rem 0 0;
  font-size: 1rem;
}

.carousel-control {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  border: none;
  padding: 1rem;
  font-size: 1.5rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.carousel-control:hover {
  background-color: rgba(0, 0, 0, 0.7);
}

.carousel-control.prev {
  left: 0;
}

.carousel-control.next {
  right: 0;
}

@media (min-width: 768px) {
  .carousel-inner {
    aspect-ratio: 21 / 9;
  }
}
</style>

