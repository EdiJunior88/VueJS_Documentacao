<script setup>
import { ref } from "vue";

const count = ref(0);

function increment() {
  // `.value` é necessário na JavaScript
  count.value++;
}
</script>

<template>
  <button @click="increment">{{ count }}</button>
</template>

<style></style>
