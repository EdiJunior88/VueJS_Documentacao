<script setup></script>

<template>
  <!-- só chama `vm.submit()` quando a `tecla` pressionada for `Enter` -->
  <input @keyup.enter="submit" />

  <!-- 
    Tu podes utilizar diretamente quaisquer nomes de tecla válidos 
    expostos através de KeyboardEvent.key como modificadores 
    convertendo-os para "kebab-case".
   -->
  <input @keyup.page-down="onPageDown" />

  <!-- Alt + Enter -->
  <input @keyup.alt.enter="clear" />

  <!-- Ctrl + Click -->
  <div @click.ctrl="doSomething">Do something</div>

  <!-- isto disparará mesmo se Alt ou Shift também for pressionado -->
  <button @click.ctrl="onClick">A</button>

  <!-- isto só disparará quando Ctrl e não outras teclas for pressionado -->
  <button @click.ctrl.exact="onCtrlClick">A</button>

  <!-- isto só disparará quando nenhum dos modificadores do sistema for pressionado -->
  <button @click.exact="onClick">A</button>
</template>

<style></style>
