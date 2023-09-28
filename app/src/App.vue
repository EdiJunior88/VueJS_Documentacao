<script setup>
import { onMounted, ref } from "vue";

/* 
Quando o ref é utilizado dentro de v-for, a referência correspondente
 deve conter uma valor de arranjo, que será povoada com os elementos 
 depois de montar:
*/

const list = ref([1, 2, 3]);
const itemRefs = ref([]);

onMounted(() => {
  alert(itemRefs.value.map((i) => i.textContent));
});
</script>

<template>
  <ul>
    <li v-for="item in list" ref="itemRefs">
      {{ item }}
    </li>
  </ul>
</template>

<style lang="css" scoped></style>
