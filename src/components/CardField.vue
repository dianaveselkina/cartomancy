<script setup></script>
<template>
  <div class="field"></div>
</template>

<style scoped>
.field {
  margin: 1rem auto;
  margin-top: 2rem;
  width: 20rem;
  height: 10rem;
  padding: 1rem;
  border-radius: 1rem;
  cursor: pointer;
  background-color: rgb(255, 255, 255);
}
.game__start:hover {
  box-shadow: 0 0 14px 14px rgba(65, 62, 21, 1.6);
}
</style>

<!-- Показать три случайных изображения

<template>
  <div>
    <h2>Случайные изображения</h2>
    <div class="image-gallery">
      <img v-for="(image, index) in randomImages" :key="index" :src="image" alt="Случайное изображение" />
    </div>
    <button @click="getRandomImages">Показать три случайных изображения</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

// Создаем реактивный массив изображений
const images = ref([
  'https://example.com/image1.jpg', 
  'https://example.com/image2.jpg',
  'https://example.com/image3.jpg',
  'https://example.com/image4.jpg',
  'https://example.com/image5.jpg',
  
]);

// Реактивная переменная для хранения случайных изображений
const randomImages = ref([]);

// Функция для получения трех случайных изображений
const getRandomImages = () => {
  const shuffledImages = images.value.sort(() => 0.5 - Math.random()); // Перемешиваем массив
  randomImages.value = shuffledImages.slice(0, 3); // Берем первые три изображения
};

// Инициализация при загрузке компонента
getRandomImages();
</script>

<style>
.image-gallery {
  display: flex;
  gap: 10px;
}

img {
  max-width: 100%;
  height: auto;
  display: block;
}
button {
  margin-top: 10px;
  padding: 10px 15px;
  font-size: 16px;
}
</style> -->
