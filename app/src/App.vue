<script setup>
import { ref } from "vue";

const ok = ref(true);
</script>

<template>
  <h1 v-show="ok">Hello!</h1>
</template>

<style></style>
