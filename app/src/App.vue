<script setup>
import { ref } from "vue";

const todos = ref([
  { name: "Roberto" },
  { name: "Eduardo" },
  { name: "Felipe" },
  { name: "Anderson" },
]);
</script>

<template>
  <ul>
    <li v-for="todo in todos" :key="todo.name">
      {{ todo.name }}
    </li>
  </ul>
</template>

<style></style>
