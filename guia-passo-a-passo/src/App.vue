<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
  //update component state
  //atualize o estado do componente
  count.value++
}
</script>

<template>
  <button @click="increment">count is: {{ count }}</button>
</template>

<style lang="css" scoped></style>
