<script setup>
import { ref, watch } from "vue";

const x = ref(0);
const y = ref(0);

/* 
O primeiro argumento do watch pode ser de diferentes 
tipos de "fontes" reativas: pode ser uma referência 
(incluindo referências computadas), um objeto reativo, 
uma função recuperada, ou um arranjo de várias fontes:
*/

/* Referência única */
watch(x, (newX) => {
  console.log(`x is ${newX}`);
});

/* Recuperador */
watch(
  () => x.value + y.value,
  (sum) => {
    console.log(`sum of x + y is: ${sum}`);
  }
);

/* arranjo de várias fontes */
watch([x, () => y.value], ([newX, newY]) => {
  console.log(`x is ${newX} and y is ${newY}`);
});
</script>

<template></template>

<style lang="css" scoped></style>
