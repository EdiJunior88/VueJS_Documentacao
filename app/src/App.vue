<script setup></script>

<template>
  <input type="checkbox" v-model="toggle" true-value="yes" false-value="no" />

  <!-- 
    A true-value e false-value são atributos específicos de Vue 
    que só funcionam com a v-model. Aqui o valor da propriedade 
    toggle será definido para 'yes' quando a caixa for confirmada, 
    e definida para 'no' quando a confirmação for desfeita. 
    Tu também podes vinculá-los à valores dinâmicos utilizando a v-bind:
   -->
  <input
    type="checkbox"
    v-model="toggle"
    :true-value="dynamicTrueValue"
    :false-value="dynamicFalseValue" />
</template>

<style lang="scss" scoped></style>
