<script setup>
/* 
É comum para a função de resposta do observador usar exatamente 
o mesmo estado reativo como fonte. Por exemplo, considere o 
seguinte código, que usa um observador para carregar um recurso 
remoto sempre que a referência todoId mudar:
*/
const todoId = ref(1);
const data = ref(null);

watch(
  todoId,
  async () => {
    const response = await fetch(
      `https://jsonplaceholder.typicode.com/todos/${todoId.value}`
    );
    data.value = await response.json();
  },
  { immediate: true }
);

/* 
Em particular, repare em como o observador usa o todoId duas vezes, 
uma vez como fonte e depois novamente dentro da função de resposta.

Isto pode ser simplificado com watchEffect(). A watchEffect() 
permite-nos rastrear as dependências reativas da função de resposta 
automaticamente. O observador acima pode ser reescrito como:
*/
watchEffect(async () => {
  const response = await fetch(
    `https://jsonplaceholder.typicode.com/todos/${todoId.value}`
  );
  data.value = await response.json();
});
</script>

<template></template>

<style lang="css" scoped></style>
