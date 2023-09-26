<script setup>
  const items = 'Hello World'
</script>

<template>
  <ul>
    <template v-for="item in items">
      <li>{{ item.msg }}</li>
      <li class="divider" role="presentation"></li>
    </template>
  </ul>
</template>

<style></style>
