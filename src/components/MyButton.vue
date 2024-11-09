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

const getRandomImage = () => {
  const randomIndex = Math.floor(Math.random() * images.value.length);
  randomImage.value = images.value[randomIndex];
};
const getRandomImage1 = () => {
  const randomIndex = Math.floor(Math.random() * images.value.length);
  randomImage1.value = images.value[randomIndex];
};
</script>
<template>
  <div>
    <button class="start" @click="getRandomImage">Start</button>
    <img
      :src="randomImage"
      v-if="randomImage"
      @click="getRandomImage1"
      class="prediction"
    />
    <img :src="randomImage1" v-if="randomImage1" class="prediction1" />
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
<!-- <template>
  <div>
    <button @click="handleClick">Нажми меня!</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

// Счетчик нажатий на кнопку
const clickCount = ref(0);

// Определяем массив функций
const functions = [
  () => {
    console.log('Первое нажатие - вызвана функция первого действия');
    // Ваш код для первого действия
  },
  () => {
    console.log('Второе нажатие - вызвана функция второго действия');
    // Ваш код для второго действия
  },
  () => {
    console.log('Третье нажатие - вызвана функция третьего действия');
    // Ваш код для третьего действия
  },
];

// Функция для обработки нажатий на кнопку
const handleClick = () => {
  const index = clickCount.value % functions.length; // Получить индекс функции
  functions[index](); // Вызвать соответствующую функцию
  clickCount.value++; // Увеличить счетчик нажатий
};
</script>

<style>
button {
  padding: 10px 15px;
  font-size: 16px;
}
</style> -->
