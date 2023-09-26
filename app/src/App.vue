<script setup>
import { ref } from "vue";
import MyComponent from "./MyComponent.vue";

const items = ref([
  { name: "Edinaldo" },
  { name: "Rozana" },
  { name: "Marinalva" },
  { name: "Ariclênio" },
  { name: "Persivaldo" },
]);
</script>

<template>
  <MyComponent
    v-for="(item, index) in items"
    :name="item.name"
    :index="index" />
</template>

<style></style>
