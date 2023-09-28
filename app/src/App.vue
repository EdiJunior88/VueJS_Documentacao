<script setup></script>

<template>
  <!-- 
    A v-model também suporta vinculações de valor de valores 
    que não são sequência de caracteres! No exemplo acima, 
    quando a opção é selecionada, selected será definida 
    para o valor literal de objeto de { number: 123 }.
   -->
  <select v-model="selected">
    <!-- inline object literal -->
    <option :value="{ number: 123 }">123</option>
  </select>
</template>

<style lang="scss" scoped></style>
