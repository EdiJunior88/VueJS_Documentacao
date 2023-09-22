<script setup>
import { reactive } from "vue";

const baseStyles = reactive({
  fontSize: "20px",
  fontWeight: "bold",
  border: "3px solid green",
});

const overridingStyles = reactive({
  color: "blue",
  letterSpacing: "0.3rem",
  padding: "20px",
});
</script>

<template>
  <div :style="[baseStyles, overridingStyles]">
    :style arranjo de vários objetos de estilo
  </div>
</template>

<style></style>
