<script setup>
function consoleLog(value) {
  console.log(value);
}

const teste = 'Este é um título de múltiplas linhas'
</script>

<template>
  <span :title="teste"> {{ consoleLog("console.log print in your browser") }} </span>
</template>

<style></style>
