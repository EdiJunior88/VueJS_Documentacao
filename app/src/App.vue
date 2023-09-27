<script setup>
import { ref } from "vue";

const name = ref("Vue.js");

function greet(event) {
  alert(`Hello ${name.value}`);

  // `event` é um evento de DOM nativo
  if (event) {
    alert(event.target.tagName);
  }
}
</script>

<template>
  <!-- `greet` é o nome do método definido acima -->
  <button @click="greet">Greet</button>
</template>

<style></style>
