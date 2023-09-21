<script setup>
const isActive = true;
const hasError = false
</script>

<template>
  <div :class="{ active: isActive }">Class Active</div>
  <div class="static" :class="{ active: isActive, 'text-danger': hasError }">Class Static Active</div>
</template>

<style></style>
