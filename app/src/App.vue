<script setup>
// const msg = "Isso é uma interpolação de texto";
const msg = "Hello World";
</script>

<template>
  <span>
    Message: <span class="msg">{{ msg }}</span>
  </span>
</template>

<style>
.msg {
  font-weight: bold;
  font-size: 1.5rem;
  color: red;
}
</style>
