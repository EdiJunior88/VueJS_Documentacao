<script setup>
const number = 50;
let test = true;
const YES = "YES";
const NO = "NO";
const message = "The quick brown fox jumps over the lazy dog.";
let id = 10;
</script>

<template>
  <p>The number {{ number }} + 1 = {{ number + 1 }}</p>
  <p :style="{ color: test ? 'red' : 'green' }">{{ test ? YES : NO }}</p>
  <p>{{ message.split("").reverse().join("") }}</p>
  <div :id="`list-${id}`"></div>
</template>

<style></style>
