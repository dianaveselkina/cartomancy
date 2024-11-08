<script setup>
import MyButton from './MyButton.vue';
</script>
<template>
  <div class="board">
    <MyButton />
  </div>
</template>

<style scoped>
.board {
  width: 450px;
  height: 594px;
  background: linear-gradient(rgba(186, 124, 55, 0.5), rgba(181, 182, 33, 0.5));
  border-radius: 10%;
  border: 4px solid #413e15;
  text-align: center;
}
</style>
