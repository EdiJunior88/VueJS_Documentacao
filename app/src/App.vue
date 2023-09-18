<script setup>
const url = "https://www.w3schools.com/vue/img_beach3.jpg";
const fontSize = "2rem";
const fontWeight = "bold";
const color = "blue";
const isButtonDisabled = true
</script>

<template>
  <p>Using v-bind in image: <img v-bind:src="url" /></p>
  <p>
    Using v-bind with abbreviation:
    <span :style="{ fontSize, fontWeight, color }">Text Example</span>
  </p>
  <p>
    Using v-bind with boolean attribute
    <button :disabled="isButtonDisabled">Button disabled</button>
  </p>
</template>

<style>
img {
  width: 40%;
}
</style>
