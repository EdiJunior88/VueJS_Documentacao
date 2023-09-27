<script setup></script>

<template>
  <!-- o propagação do evento de clique será interrompida -->
  <a @click.stop="doThis"></a>

  <!-- o evento de submeter já não recarregará a página -->
  <form @submit.prevent="onSubmit"></form>

  <!-- modificadores podem ser encadeados -->
  <a @click.stop.prevent="doThat"></a>

  <!-- apenas o modificador -->
  <form @submit.prevent></form>

  <!-- apenas aciona o manipulador se `event.target` for o próprio elemento -->
  <!-- por exemplo, não um elemento filho -->
  <div @click.self="doThat">...</div>

  <!-- utilize o modo de captura quando estiveres adicionando o ouvinte de evento -->
  <!-- por exemplo, um evento mirando um elemento interno é manipulado aqui antes de ser manipulado por aquele elemento -->
  <div @click.capture="doThis">...</div>

  <!-- o evento de clique será acionado no máximo uma vez -->
  <a @click.once="doThis"></a>

  <!-- o comportamento padrão do evento de deslocamento (deslocando) acontecerá -->
  <!-- imediatamente, no lugar de esperar o `onScroll` terminar  -->
  <!-- neste caso ele contém `event.preventDefault()`                -->
  <div @scroll.passive="onScroll">...</div>
</template>

<style></style>
