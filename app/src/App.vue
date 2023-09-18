<script setup>
const rawHTML = "This should be red";
</script>

<template>
  <p>
    Using text interpolation <span style="color: red">{{ rawHTML }}</span>
  </p>
  <p>Using v-html directive: <span v-html="rawHTML"></span></p>
</template>

<style>
span {
  color: blue;
}
</style>
