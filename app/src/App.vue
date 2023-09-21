<script setup>
let state = reactive({ count: 0 });

// a referência acima ({ count: 0 }) não está mais a ser rastreada
// (conexão da reatividade está perdida!)
state = reactive({ count: 1 });

/* --------------------------------------------------------------------- */

const state2 = reactive({ count: 0 });

// `count` está desconectado da `state.count` quando desestruturada.
let { count } = state2.count;
// não afeta o estado original
count++;

// a função recebe um número simples e
// não será capaz de rastrear as mudanças para `state.count`
// temos de passar o objeto inteiro para reter a reatividade
callSomeFunction(state2.count);
</script>

<template></template>

<style></style>
