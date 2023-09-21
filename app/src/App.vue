<script setup>
import { reactive } from "vue";

const raw = {};
const proxy = reactive(raw);

// a delegação NÃO é igual ao original.
console.log(proxy === raw); //false

// a chamada de reactive() sobre o mesmo objeto retorna a mesma delegação
console.log(reactive(raw) === proxy); //true

// a chamada de reactive() sobre uma delegação retorna a si mesma
console.log(reactive(proxy) === proxy); //true

const proxy2 = reactive({});

const raw2 = {};
proxy2.nested = raw;
console.log(proxy2.nested === raw); //false
</script>

<template></template>

<style></style>
