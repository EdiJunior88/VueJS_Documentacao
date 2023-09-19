<script setup>
const blue = true;
</script>

<template>
  <p v-if="blue" :style="{ color: 'blue' }">This text will be blue</p>
  <p v-else="red" :style="{ color: 'red' }">This text will be red</p>
</template>

<style></style>
