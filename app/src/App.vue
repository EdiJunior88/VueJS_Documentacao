<script setup>
import { computed, ref } from "vue";

const firstName = ref("John");
const lastName = ref("Doe");

const fullName = computed({
  //recuperador
  get() {
    return firstName.value + " " + lastName.value;
  },

  //definidor
  set(newValue) {
    // Nota: nós estamos utilizando a sintaxe de atribuição de desestruturação.
    [firstName.value, lastName.value] = newValue.split(" ");
  },
});
</script>

<template>
  <p>Full Name:</p>
  <span>{{ fullName }}</span>
</template>

<style></style>
