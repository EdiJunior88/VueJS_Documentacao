<script setup>
import { reactive, ref } from "vue";

const activeColor = ref("red");
const fontSize = ref(30);

//Frequentemente é uma boa ideia vincular a um objeto de estilo diretamente
//para que o modelo de marcação esteja mais limpo:
const styleObject = reactive({
  color: "red",
  fontSize: "13px",
});
</script>

<template>
  <div :style="{ color: activeColor, fontSize: fontSize + 'px' }">:style</div>
  <div :style="{ 'font-size': fontSize + 'px' }">
    :style CSS em "kebab-case"
  </div>
  <div :style="styleObject">:style vincular a um objeto de estilo</div>
</template>

<style></style>
