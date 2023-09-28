<script setup></script>

<template>
  <!-- 
    O pick será definido para o valor de first quando 
    a primeira entrada de rádio for confirmada, e 
    definida para o valor de second quando o segundo 
    for confirmado.
   -->
  <input type="radio" v-model="pick" :value="first" />
  <input type="radio" v-model="pick" :value="second" />
</template>

<style lang="scss" scoped></style>
