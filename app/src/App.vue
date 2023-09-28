<script setup>
import { onMounted } from "vue";

onMounted(() => {
  console.log(`The component is now mounted`);
});
</script>

<template>
  <!-- 
    Quando estiveres chamando onMounted, a Vue associa 
    automaticamente a função de resposta registada com 
    a atual instância do componente ativo. Isto exige 
    que estes gatilhos sejam registados de forma síncrona 
    durante a definição de componente.
   -->
</template>

<style lang="scss" scoped></style>
