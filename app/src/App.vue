<script setup>
import { ref } from "vue";

const message = ref("");
</script>

<template>
  <span>Multiline message is:</span>
  <p>{{ message }}</p>

  <!-- 
    Nota que a interpolação dentro de <textarea> não funcionará. Utilize v-model.
 -->
  <textarea v-model="message" placeholder="add multiples lines"></textarea>
</template>

<style>
p {
  white-space: pre-line;
}
</style>
