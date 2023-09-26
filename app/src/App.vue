<script setup>
import { reactive } from "vue";

const myObject = reactive({
  title: "How to do lists in Vue",
  author: "Jane Doe",
  publishedAt: "2016-04-10",
});
</script>

<template>
  <ul>
    <li v-for="value in myObject">
      {{ value }}
    </li>
  </ul>

  <!-- 
    Tu também podes fornecer um segundo pseudônimo 
    para o nome da propriedade (também conhecido como chave):
   -->

  <ul>
    <li v-for="(value, key) in myObject">{{ key }}: {{ value }}</li>
  </ul>

  <!-- 
    E um outro para o índice:
   -->

  <ul>
    <li v-for="(value, key, index) in myObject">
      {{ index }}. {{ key }}: {{ value }}
    </li>
  </ul>
</template>

<style></style>
