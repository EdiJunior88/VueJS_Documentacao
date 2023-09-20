<script setup>
import { ref } from "vue";

const obj = ref({
  nested: { count: 0 },
  arr: ["foo", "bar"],
});

function mutateDeeply() {
  obj.value.nested.count++;
  console.log("obj.value.nested.count++ = " + obj.value.nested.count++);
  
  obj.value.arr.push("baz");
  console.log("obj.value.arr.push('baz') = " + obj.value.arr);
}

mutateDeeply();
</script>

<template></template>

<style></style>
