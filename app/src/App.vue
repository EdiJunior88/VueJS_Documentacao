<script setup>
import { ref } from "vue";

const checked = ref(true);

/* 
  Nós também podemos vincular várias caixas de confirmação 
  ao mesmo valor de arranjo ou conjunto: 
*/
const checkedNames = ref([]);
</script>

<template>
  <input type="checkbox" id="checkbox" v-model="checked" />
  <label for="checkbox">{{ checked }}</label>

  <!-- 
    Neste caso, o arranjo checkedNames sempre conterá 
    os valores das caixas confirmadas atualmente.
   -->
  <div>Checked names: {{ checkedNames }}</div>

  <input type="checkbox" id="jack" value="jack" v-model="checkedNames" />
  <label for="jack">Jack</label>

  <input type="checkbox" id="john" value="john" v-model="checkedNames" />
  <label for="john">John</label>

  <input type="checkbox" id="mike" value="mike" v-model="checkedNames" />
  <label for="mike">Mike</label>
</template>

<style></style>
