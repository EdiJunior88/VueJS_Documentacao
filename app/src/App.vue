<script setup>
import { computed, ref } from "vue";

const numbers = ref([1, 2, 3, 4, 5]);

const sets = ref([
  [1, 2, 3, 4, 5],
  [6, 7, 8, 9, 10],
]);

function even(numbers) {
  return numbers.filter((number) => number % 2 === 0);
}

const eventNumbers = computed(() => {
  return numbers.value.filter((n) => n % 2 === 0);
});
</script>

<template>
  <li v-for="n in eventNumbers">{{ n }}</li>

  <br />

  <!-- Em situações onde as propriedades computadas não são viáveis 
    (por exemplo, dentro de laços v-for encaixados), podes utilizar um método: 
  -->

  <ul v-for="numbers in sets">
    <li v-for="n in even(numbers)">{{ n }}</li>
  </ul>
</template>

<style></style>
