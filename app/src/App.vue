<script setup>
import { computed, reactive } from "vue";

const author = reactive({
  name: "John Doe",
  books: [
    "Vue 2 - Advanced Guide",
    "Vue 3 - Basic Guide",
    "Vue 4 - The Mystery",
  ],
});

/* Neste ponto, o modelo de marcação está ficando um pouco desarrumado. 
Nós precisamos olhar nele por um segundo antes de perceber que ela realiza 
um cálculo dependendo de author.books. Mais importante, nós provavelmente 
não queremos nos repetir se precisarmos incluir este cálculo no modelo de 
marcação mais de uma vez.

É por isto que para lógica complexa que inclui dados reativos, é recomendado 
utilizar uma propriedade computada. */

// uma referência computada
const publishedBooksMessage = computed(() => {
  return author.books.length > 0 ? "YES" : "NO";
});
</script>

<template>
  <!-- E quisermos exibir mensagens diferentes caso o author tiver alguns livros ou não: -->
  <p>Has published books:</p>
  <span>{{ publishedBooksMessage }}</span>
</template>

<style></style>
