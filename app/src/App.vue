<script setup>
/* 
O watch é preguiçoso por padrão: a resposta não será chamada 
até que a fonte observada tenha mudado. Mas em alguns casos 
podemos querer que a mesma lógica de resposta seja executada 
incansavelmente - por exemplo, podemos querer pedir alguns 
dados iniciais, e depois pedir novamente os dados sempre que 
o estado relevante mudar.

Nós podemos forçar uma resposta do observador a ser executada 
imediatamente passando a opção immediate: true:
*/
watch(
  source,
  (newValue, oldValue) => {
    // executado imediatamente, depois novamente quando `source` mudar
  },
  { immediate: true }
);
</script>

<template></template>

<style lang="css" scoped></style>
