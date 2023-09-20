<script setup>
import { nextTick, ref } from "vue";

const count = ref(0);

async function increment() {
  count.value++;

  // DOM ainda não foi atualizado
  console.log(document.getElementById("counter").textContent); //0

  await nextTick();
  // DOM agora está atualizado
  console.log(document.getElementById("counter").textContent); //1
}
</script>

<template>
  <button id="counter" @click="increment">{{ count }}</button>
</template>

<style></style>
