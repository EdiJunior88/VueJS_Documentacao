<script setup>
/* 
Como verás acima, utilizamos o <slot> como um espaço reservado 
onde queremos que conteúdo esteja – e é isto. Terminamos!
*/
</script>

<template>
  <div class="alert-box">
    <strong>Error</strong>
    <br />
    <slot />
  </div>
</template>

<style lang="css" scoped>
.alert-box {
  color: #666;
  border: 1px solid red;
  border-radius: 4px;
  padding: 20px;
  background-color: #f8f8f8;
}

strong {
  color: red;
}
</style>
