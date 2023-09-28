<script setup>
import { ref, watch } from "vue";

const question = ref("");
const answer = ref("Questions usually contai a question mark. ;-)");

// `watch` trabalha diretamente sobre uma referência
watch(question, async (newQuestion, oldQuestion) => {
  if (newQuestion.indexOf("?") > -1) {
    answer.value = "Thinking...";

    try {
      const res = await fetch("https://yesno.wtf/api");
      answer.value = (await res.json()).answer;
    } catch (error) {
      answer.value = "Error! could not reach the API. " + error;
    }
  }
});
</script>

<template>
  <p>
    Ask a yes/no question:
    <input v-model="question" />
  </p>
  <p>{{ answer }}</p>
</template>

<style lang="css" scoped></style>
