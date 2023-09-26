<script setup>
import { ref } from "vue";

const items = ref([
  {
    message: "Foo",
  },
  {
    message: "Bar",
  },
]);

const parentMessage = ref("Parent");
</script>

<template>
  <li v-for="(item, index) in items">
    {{ parentMessage }} - {{ index }} - {{ item.message }}
  </li>

  <!-- 
    Dentro do escopo de v-for, as expressões do modelo de marcação tem 
    acesso a todas propriedades do escopo do pai. Além disto, a v-for 
    também suporta um segundo pseudônimo opcional para índice do item atual:
   -->

  <!-- 
    O escopo de variável da v-for é similar ao seguinte código de JavaScript:

    const parentMessage = 'Parent'
    const items = [
      /* ... */
    ]

    items.forEach((item, index) => {
      // tem acesso ao `parentMessage` do escopo externo 
      // mas `item` e `index` apenas estão disponíveis aqui
      console.log(parentMessage, item.message, index)
    })
    -->
</template>

<style></style>
