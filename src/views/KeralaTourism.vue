<template>
  <div class="kerala-tourism">
    <Header :navLinks="navLinks" />
    <div class="main-content">
      <div class="layout-content-container">
        <HeroSection />
        <AboutSection />
        <FestivalHighlights />
        <ImageGallery />
        <OnamEvents />
        <CTASection />
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import HeroSection from '@/components/HeroSection.vue'
import AboutSection from '@/components/AboutSection.vue'
import FestivalHighlights from '@/components/FestivalHighlights.vue'
import ImageGallery from '@/components/ImageGallery.vue'
import OnamEvents from '@/components/OnamEvents.vue'
import CTASection from '@/components/CTASection.vue'

export default {
  name: 'KeralaTourism',
  components: {
    Header,
    HeroSection,
    AboutSection,
    FestivalHighlights,
    ImageGallery,
    OnamEvents,
    CTASection
  },
  data() {
    return {
      navLinks: ['Explore', 'Travel', 'Festivals', 'Destinations', 'Experiences', 'Blog'],
      festivalHighlights: [
        { title: 'Festival of Harvest', description: 'Celebrated in Kerala', image: 'https://cdn.usegalileo.ai/sdxl9/2119a052-e8f0-4208-8394-c49aeae03cf1.png' },
        { title: 'Joyous Celebrations', description: 'Feasting, boat races', image: 'https://cdn.usegalileo.ai/sdxl9/39f972fa-758d-4f87-8e2c-755947ebbbc0.png' },
        { title: 'Music and Dance', description: 'Performances in temples', image: 'https://cdn.usegalileo.ai/sdxl9/61ef8b5d-523b-40dc-958b-a5c73a98dd8a.png' },
        { title: 'Floral Designs', description: 'Pookalam adorns floors', image: 'https://cdn.usegalileo.ai/sdxl9/4869abb1-d304-42b4-b8cd-89efe42c8675.png' }
      ],
     
    }
  }
}
</script>

<style scoped>
.kerala-tourism {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  background-color: white;
  overflow-x: hidden;
}

.main-content {
  padding: 1.25rem 10rem;
  display: flex;
  flex: 1;
  justify-content: center;
}

.layout-content-container {
  display: flex;
  flex-direction: column;
  max-width: 960px;
  flex: 1;
}

.events-title {
  color: #181611;
  font-size: 1.375rem;
  font-weight: 700;
  line-height: 1.25;
  letter-spacing: -0.015em;
  padding: 1.25rem 1rem 0.75rem;
}
</style>
