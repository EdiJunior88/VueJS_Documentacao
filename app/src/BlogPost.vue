<script setup>
defineProps(["title"]);

/* 
Nós podemos opcionalmente declarar eventos emitidos utilizando a macro defineEmits:
*/
const emit = defineEmits(["enlarge-text"]);
</script>

<template>
  <h4>{{ title }}</h4>
  <button @click="$emit('enlarge-text')">Enlarge text</button>
  <button @click="emit('enlarge-text')">Enlarge Text With defineEmits</button>
</template>

<style lang="css" scoped></style>
