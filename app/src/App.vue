<script setup>
import { ref } from "vue";

const picked = ref("");
const toggle = ref("");
const selected = ref("");
</script>

<template>
  <!-- `picked` é uma sequência de carácter "a" quando for confirmada -->
  <input type="radio" v-model="picked" value="a" />

  <!-- `toggle` é ou verdadeiro ou é falso -->
  <input type="checkbox" v-model="toggle" />

  <!-- `selected` é uma sequência de caracteres "abc" quando a primeira opção for selecionada -->
  <select v-model="selected">
    <option value="abc">ABC</option>
  </select>
</template>

<style lang="scss" scoped></style>
