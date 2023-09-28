<script setup>
/* 
Quando alterares o estado reativo, ele pode acionar 
tanto as atualizações de componente de Vue e respostas 
de observador criadas por ti.

Por padrão, respostas de observador criadas pelo utilizador 
são chamadas antes das atualização de componente de Vue. Isto 
significa que se tentares acessar o DOM de dentro de uma 
resposta de observador, o DOM estará no estado antes da Vue 
tiver aplicado quaisquer atualizações.

Se quiseres acessar o DOM em uma resposta de observador depois 
da Vue tiver atualizado-o, precisas especificar a opção flush: 'post':
*/
watch(source, callback, {
  flush: "post",
});

watchEffect(callback, {
  flush: "post",
});

/* 
A watchEffect() pós-fluxo também tem um pseudônimo de conveniência, 
watchPostEffect():
*/
import { watchPostEffect } from "vue";

watchPostEffect(() => {
  /* executada depois das atualizações de Vue */
});
</script>

<template></template>

<style lang="css" scoped></style>
