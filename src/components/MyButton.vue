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
  '/img/card8.png',
  '/img/card9.png',
  '/img/card10.png',
  '/img/card11.png',
  '/img/card12.png',
  '/img/card13.png',
  '/img/card14.png',
  '/img/card15.png',
  '/img/card16.png',
  '/img/card17.png',
  '/img/card18.png',
  '/img/card19.png',
  '/img/card20.png',
  '/img/card21.png',
  '/img/card22.png',
]);

const randomImage = ref('');
const randomImage1 = ref('');
const randomImage2 = ref('');
const randomImage3 = ref('');
const clickCount = ref(0);

const functions = [
  () => {
    const randomIndex = Math.floor(Math.random() * images.value.length);
    randomImage1.value = images.value[randomIndex];
  },
  () => {
    const randomIndex = Math.floor(Math.random() * images.value.length);
    randomImage2.value = images.value[randomIndex];
  },
  () => {
    const randomIndex = Math.floor(Math.random() * images.value.length);
    randomImage3.value = images.value[randomIndex];
  },
];

const handleClick = () => {
  const index = clickCount.value % functions.length;
  functions[index]();
  clickCount.value++;
};
const getRandomImage = () => {
  const randomIndex = Math.floor(Math.random() * images.value.length);
  randomImage.value = images.value[randomIndex];
};
</script>
<template>
  <div>
    <button class="start" @click="getRandomImage"></button>
    <img
      :src="randomImage"
      v-if="randomImage"
      @click="handleClick"
      class="prediction"
    />
  </div>
  <div class="prediction__block">
    <img :src="randomImage1" v-if="randomImage1" class="prediction1" />
    <img :src="randomImage2" v-if="randomImage2" class="prediction2" />
    <img :src="randomImage3" v-if="randomImage3" class="prediction3" />
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
.prediction__block {
  margin: 1rem auto;
  margin-top: 2rem;
  width: 20rem;
  height: 10rem;
  padding: 1rem;
  border-radius: 1rem;
  background-color: rgb(255, 255, 255);
  display: block;
}
.prediction {
  cursor: pointer;
}
.prediction1 {
  position: absolute;
  top: 29rem;
  left: 50%;
  transform: translate(-50%);
  width: 6rem;
  height: 8rem;
}
.prediction2 {
  position: absolute;
  top: 29rem;
  left: 40%;
  transform: translate(-50%);
}
.prediction3 {
  position: absolute;
  top: 29rem;
  left: 60%;
  transform: translate(-50%);
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
