<script setup>
import { ref } from "vue";

const count = ref(0);

/* console.log(count); //{value: 0}
console.log(count.value); //0

count.value++;
console.log(count.value); //1 */
</script>

<template>
  <button @click="count++">{{ count }}</button>
</template>

<style></style>
