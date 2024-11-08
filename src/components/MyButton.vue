<script setup>
import { ref } from 'vue';
const prizeVisibility = ref(false);
const showPrize = () => {
  prizeVisibility.value = true;
};
</script>
<template>
  <div>
    <button class="start" @click="showPrize()">Start</button>
    <transition name="showPrize">
      <div class="prize" v-if="prizeVisibility">
        <div class="prize-image"></div>
      </div>
    </transition>
  </div>
</template>

<style scoped>
.start {
  margin-top: 12rem;
  width: 24rem;
  height: 32rem;
  padding: 1rem;
  border-radius: 1rem;
  cursor: pointer;
  background-color: rgba(181, 182, 33, 0.7);
  border: 4px solid #413e15;
  font-size: 3rem;
  color: #472f14;
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
  background-image: url(/public/img/test.png);
  background-repeat: no-repeat;
  background-size: cover;
  border-radius: 24px;
  z-index: 20;
  position: absolute;
  top: 65rem;
  left: 50%;
  transform: translate(-50%);
  width: 490px;
  height: 470px;
}
</style>
