<script setup>
const obj = reactive({ count: 0 });

watch(obj, (newValue, oldValue) => {
  // dispara sobre mutações de propriedade encaixada
  // Nota: cá `newValue` será igual ao `oldValue`
  // porque ambos eles apontam para o mesmo objeto!
});

obj.count++;

/* 
Isto deve ser distinguido de um recuperador que retorna 
um objeto reativo - no recente caso, a resposta só disparará 
se o recuperador retornar um objeto diferente:
*/
watch(
  () => state.someObject,
  () => {
    // dispara só quando `state.someObject` for substituído
  }
);

/* 
Tu podes, no entanto, forçar o segundo caso para um observador 
profundo utilizando explicitamente a opção deep:
*/
watch(
  () => state.someObject,
  (newValue, oldValue) => {
    // Nota: cá `newValue` será igual ao `oldValue`
    // *a menos que* `state.someObject` tenha sido substituído
  },
  { deep: true }
);
</script>

<template></template>

<style lang="css" scoped></style>
