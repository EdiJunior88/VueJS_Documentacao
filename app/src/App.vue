<script setup>
import { reactive, ref } from "vue";

const books = reactive([ref("Vue 3 Guide")]);
// neste caso precisas de `.value`
console.log(books[0].value);

const map = reactive(new Map([["count", ref(0)]]));
// neste caso precisas de `.value`
console.log(map.get("count").value);
</script>

<template></template>

<style></style>
