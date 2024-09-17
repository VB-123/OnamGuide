<script setup>
  const img1 = import('@/assets/images.jpeg');
  const img2 = import('@/assets/celeb.jpeg');
  const img3 = import('@/assets/temple.jpeg');
  const img4 = import('@/assets/pookalam.jpeg');

</script>
<template>
  <div class="festival-highlights">
    <div v-for="highlight in festivalHighlights" :key="highlight.title" class="highlight-card">
      <div class="highlight-image" :style="{ backgroundImage: `url(${highlight.image})` }"></div>
      <div>
        <p class="highlight-title" >{{ highlight.title }}</p>
        <p class="highlight-description">{{ highlight.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FestivalHighlights',
  props: {
    highlights: {
      type: Array,
      required: true
    }
  },
  data(){
    return{
      festivalHighlights:[
        { title: 'Festival of Harvest', description: 'Celebrated in Kerala', image: img1 },
        { title: 'Joyous Celebrations', description: 'Feasting, boat races', image: img2 },
        { title: 'Music and Dance', description: 'Performances in temples', image: img3 },
        { title: 'Floral Designs', description: 'Pookalam adorns floors', image: img4 }
      ]
    }
  }
}
</script>

<style scoped>
.festival-highlights {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(158px, 1fr));
  gap: 0.75rem;
}
.highlight-card {
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
  padding-bottom: 0.75rem;
}

.highlight-image {
  width: 100%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  border-radius: 0.75rem;
  aspect-ratio: 16 / 9;
}

.highlight-title {
  color: #181611;
  font-size: 1rem;
  font-weight: 500;
  line-height: normal;
}

.highlight-description{
  color: #8a7c60;
  font-size: 0.875rem;
  font-weight: 400;
  line-height: normal;
}

.highlight-card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.highlight-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.highlight-image {
  transition: transform 0.3s ease;
}

.highlight-card:hover .highlight-image {
  transform: scale(1.05);
}

</style>
