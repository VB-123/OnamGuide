<template>
    <h2 class="events-title">Onam Events</h2>      
    <div class="onam-events">
      <div v-for="event in onamEvents" :key="event.title" class="event-card">
        <div class="event-image" :style="{ backgroundImage: `url(${event.image})` }">
        </div>
        <div>
          <p class="event-title">{{ event.title }}</p>
          <p class="event-description">{{ event.description }}</p>
        </div>
      </div>
    </div>
</template>
<script>
export default {
  name: 'OnamEvents',
  data(){
    return{
      onamEvents: [
          { title: 'Onam Sadhya', description: 'Grand feast', image: 'https://cdn.usegalileo.ai/sdxl10/dbb12340-0563-42b0-9f50-949077b05f18.png' },
          { title: 'Pulikali', description: 'Tiger dance', image: 'https://cdn.usegalileo.ai/sdxl10/6560c96f-56c5-4984-a776-5a029ff8a29c.png' },
          { title: 'Vallamkali', description: 'Snake boat race', image: 'https://cdn.usegalileo.ai/sdxl10/9355d238-ce1f-4e27-9c60-5c13c1828c7d.png' }
      ]
    }
  }
}
</script>

<style scoped>
.onam-events {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(158px, 1fr));
  gap: 0.75rem;
}

.events-title {
  color: #181611;
  font-size: 1.375rem;
  font-weight: 700;
  line-height: 1.25;
  letter-spacing: -0.015em;
  padding: 1.25rem 1rem 0.75rem;
}

.event-card {
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
  padding-bottom: 0.75rem;
}

.event-card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.event-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.event-image {
  transition: transform 0.3s ease;
}

.event-card:hover .event-image {
  transform: scale(1.05);
}

.event-image {
  width: 100%;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  border-radius: 0.75rem;
  aspect-ratio: 16 / 9;
}

.event-title {
  color: #181611;
  font-size: 1rem;
  font-weight: 500;
  line-height: normal;
}

.event-description {
  color: #8a7c60;
  font-size: 0.875rem;
  font-weight: 400;
  line-height: normal;
}

</style>
