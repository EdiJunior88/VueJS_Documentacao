<script setup></script>

<template>
  <!-- 
    Por padrão, a v-model sincroniza a entrada com o dado 
    depois de cada evento de input (com a exceção da 
    composição de IME como especificada acima). Tu podes 
    adicionar o modificador lazy no lugar de sincronizar 
    depois dos eventos change:
   -->
  <!-- sincronizado depois de "change" no lugar de "input" -->
  <input v-model.lazy="msg" />
</template>

<style lang="scss" scoped></style>
