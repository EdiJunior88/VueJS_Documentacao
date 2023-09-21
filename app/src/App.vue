<script setup>
import { reactive, ref } from "vue";

const count = ref(0);
const state = reactive({ count });

console.log(state.count); //0

state.count = 1;
console.log(count.value); //1

const otherCount = ref(2)

state.count = otherCount
console.log(state.count) //2;

// a referência original agora está desconectada da `state.count`
console.log(count.value);
</script>

<template></template>

<style></style>
