<script setup>
import CardField from './CardField.vue';
import MyButton from './MyButton.vue';
</script>
<template>
  <div class="board">
    <MyButton />
    <CardField />
  </div>
</template>

<style scoped>
.board {
  margin: 2rem auto;
  width: 112rem;
  height: 148rem;
  background: linear-gradient(rgba(186, 124, 55, 0.5), rgba(181, 182, 33, 0.5));
  border-radius: 10%;
  border: 15% solid #413e15;
  text-align: center;
}
</style>
