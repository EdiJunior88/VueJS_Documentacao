<script setup>
// agora temos acesso ao evento nativo
function warn(message, event) {
  if (event) {
    event.preventDefault();
  }
  alert(message);
}
</script>

<template>
  <!-- utilizando a variável especial $event -->
  <button @click="warn('Form cannot be submitted yet.', $event)">Submit</button>

  <!-- utilizando a função em flecha em linha -->
  <button @click="(event) => warn('Form cannot be submitted yet.')">
    Submit
  </button>
</template>

<style></style>
