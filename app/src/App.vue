<script setup>
const isActive = true;
const activeClass = "active";
const errorClass = "text-danger";
</script>

<template>
  <div :class="[activeClass, errorClass]">Active Text-Danger</div>
  <div :class="[isActive ? activeClass : '', errorClass]">
    Active Text-Danger
  </div>
</template>

<style></style>
