
<script setup>
import Card from 'primevue/card';

const images = [
  { src: '/img/lake-michigan.jpg', title: 'Lake Michigan'},
  { src: '/img/forest.jpg', title: 'Forest'},
  { src: '/img/sunset.jpg', title: 'Sunset'},
  { src: '/img/butterfly.jpg', title: 'Butterfly'},
  { src: '/img/flower.jpg', title: 'Flower'},
  { src: '/img/lollipop.jpg', title: 'Lollipop'}
];

</script>

<template>
    <div class="gallery">
        <Card v-for="(image, index) in images" :key="index" class="image-card">
      <template #header>
        <img :src="image.src" :alt="image.title" class="card-image" />
      </template>
      <template #title>
        {{ image.title }}
      </template>
      <template #content>
        <p>{{ image.description }}</p>
      </template>
    </Card>  
    </div>
</template>

<style scoped>

.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); 
  gap: 16px;
  padding: 20px;
  justify-items: center; 
}

.image-card {
  width: 250px;
  text-align: center;
}

.card-image {
  width: 100%;
  height: 150px;
  object-fit: cover;
  border-radius: 5px;
}
</style>

