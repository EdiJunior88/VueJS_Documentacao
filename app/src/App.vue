<script setup>
import { ref } from "vue";

const selected = ref("");
const selected2 = ref([]);
const selected3 = ref("A");
const options = ref([
  { text: "One", value: "A" },
  { text: "Two", value: "B" },
  { text: "Three", value: "C" },
]);
</script>

<template>
  <div>Selected: {{ selected }}</div>

  <select v-model="selected">
    <option disabled value="">Please select one</option>
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>

  <!-- 
    Seleção de várias escolhas (vinculadas ao arranjo (array)):
   -->
  <div>Selected: {{ selected2 }}</div>

  <select v-model="selected2" multiple>
    <option>A</option>
    <option>B</option>
    <option>C</option>
  </select>

  <!-- 
    As opções do elemento de seleção podem ser dinamicamente 
    interpretadas com a v-for:
   -->
  <select v-model="selected3">
    <option v-for="option in options" :value="option.value">
      {{ option.text }}
    </option>
  </select>

  <div>Selected: {{ selected3 }}</div>
</template>

<style>
select[multiple] {
  width: 100px;
}
</style>
