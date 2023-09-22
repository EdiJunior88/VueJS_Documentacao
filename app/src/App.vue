<script setup>
import { ref } from "vue";

const awesome = ref(true);
const ok = true;
</script>

<template>
  <button @click="awesome = !awesome">Toggle</button>

  <h1 v-if="awesome">Vue is Awesome!</h1>
  <h1 v-else>Oh no 😢</h1>

  <!-- ************************************************ -->

  <div v-if="type === 'A'">A</div>

  <div v-else-if="type === 'B'">B</div>

  <div v-else-if="type === 'C'">C</div>

  <div v-else>Not A/B/C</div>

  <!-- ************************************************ -->

  <template v-if="ok">
    <h1>Title</h1>
    <p>Paragraph 1</p>
    <p>Paragraph 2</p>
  </template>
</template>

<style></style>
