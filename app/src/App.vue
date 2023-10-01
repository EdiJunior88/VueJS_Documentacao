<script setup>
/* 
Alguns elementos de HTML, tais como <ul>, <ol>, <table> e <select> 
têm restrições sobre quais elementos podem aparecer dentro deles, 
e alguns elementos tais como <li>, <tr>, e <option> só podem 
aparecer dentro certos elementos.

Isto levará a problemas quando estiveres utilizando componentes com 
elementos que têm tais restrições. Por exemplo:

<table>
  <blog-post-row></blog-post-row>
</table>

O componente personalizado <blog-post-row> será levantado como conteúdo 
inválido, causando erros no resultado interpretado final. Nós podemos 
utilizar o atributo is especial como uma solução:

<table>
  <tr is="vue:blog-post-row"></tr>
</table>
*/
</script>

<template></template>

<style lang="css" scoped></style>
