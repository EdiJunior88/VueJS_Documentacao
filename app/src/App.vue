<script setup></script>

<template>
  <!-- 
    Se quiseres que a entrada do utilizador seja automaticamente 
    tratada como um número, podes adicionar o modificador number 
    as tuas entradas geridas pela v-model:
   -->
  <input v-model.number="age" />
  <!-- 
    Se o valor não puder ser analisado com parseFloat(), então 
    o valor original é utilizado no lugar. O modificador number 
    é aplicado automaticamente se a entrada tiver o type="number".
   -->
</template>

<style lang="scss" scoped></style>
