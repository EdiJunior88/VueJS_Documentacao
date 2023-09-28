<script setup>
import { onMounted, ref } from "vue";

/* 
Para obter a referência com a API de Composição, 
precisamos declarar uma ref com o mesmo nome:
*/

// declara uma `ref` para segurar a referência de elemento
// o nome deve corresponder ao valor de `ref` do modelo de marcação 
const input = ref(null);

onMounted(() => {
  input.value.focus();
});
</script>

<template>
  <input ref="input" />
</template>

<style lang="css" scoped></style>
