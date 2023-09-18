<script setup>
const objectOfAttrs = {
  id: "container",
  class: "wrapper",
};
</script>

<template>
  <div v-bind="objectOfAttrs">div > id: "container" / class: "wrapper"</div>
</template>

<style>
img {
  width: 40%;
}
</style>
