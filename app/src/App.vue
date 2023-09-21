<script setup>
import { reactive, ref } from "vue";

//No exemplo abaixo, count e object são propriedades de alto nível, mas object.id não:
const count = ref(0);
const object = { id: ref(1) };

//Para corrigir isto, podemos desestruturar id à uma propriedade de alto nível:
const { id } = object;
</script>

<template>
  <!-- Portanto, esta expressão funciona como esperado: -->
  {{ count + 1 }}

  <br />

  <!-- ...enquanto isto NÃO: -->
  {{ object.id + 1 }}

  <br />

  {{ id + 1 }}

  <br />

  <!-- Um outra coisa à notar é que uma referência é desembrulhada 
    se for o valor avaliado final duma interpolação de texto 
    (por exemplo, um marcador {{ }}, então o seguinte exemplo desenhará 1) -->
  {{ object.id }}

  <!-- Isto é apenas um funcionalidade de conveniência da interpolação de texto 
  e é equivalente ao {{ object.id.value }}. -->
</template>

<style></style>
