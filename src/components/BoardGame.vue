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
  margin: 1rem auto;
  width: 28rem;
  height: 48rem;
  background: linear-gradient(rgba(186, 124, 55, 0.5), rgba(181, 182, 33, 0.5));
  border-radius: 5%;
  text-align: center;
}
</style>
