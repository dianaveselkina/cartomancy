<script setup>
import { ref } from 'vue';

const images = ref([
  '/img/card1.png',
  '/img/card2.png',
  '/img/card3.png',
  '/img/card4.png',
  '/img/card5.png',
  '/img/card6.png',
  '/img/card7.png',
  '/img/test.png',
]);

const randomImage = ref('');

const getRandomImage = () => {
  const randomIndex = Math.floor(Math.random() * images.value.length);
  randomImage.value = images.value[randomIndex];
};
</script>
<template>
  <div>
    <button class="start" @click="getRandomImage">Start</button>

    <img :src="randomImage" v-if="randomImage" />
  </div>
</template>

<style scoped>
.start {
  margin-top: 2rem;
  width: 6rem;
  height: 8rem;
  border-radius: 1rem;
  cursor: pointer;
  background-color: rgba(181, 182, 33, 0.7);
  border: 4px solid #413e15;
  font-size: 1rem;
  color: #472f14;
}
img {
  position: absolute;
  top: 15rem;
  left: 50%;
  transform: translate(-50%);
  width: 6rem;
  height: 8rem;
}
.game__start:hover {
  box-shadow: 0 0 14px 14px rgba(65, 62, 21, 1.6);
}
.showPrize-enter-active,
.showPrize-leave-active {
  opacity: 1;
  transition: all 3s;
}
.showPrize-enter-from,
.showPrize-leave-to {
  opacity: 0;
}
.prize-image {
  background-repeat: no-repeat;
  background-size: cover;
  border-radius: 1rem;
  z-index: 20;
  position: absolute;
  top: 15rem;
  left: 50%;
  transform: translate(-50%);
  width: 6rem;
  height: 8rem;
}
</style>
