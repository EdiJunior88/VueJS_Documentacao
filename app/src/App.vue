<script setup>
function alertMessage() {
  alert("YES! you clicked on me!!!! :-D");
}
</script>

<template>
  <button v-on:click="alertMessage">Click</button>
</template>

<style></style>
