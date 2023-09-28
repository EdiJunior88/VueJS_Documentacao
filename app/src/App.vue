<script setup>
/* 
O ref também pode ser utilizado sobre um componente filho. 
Neste caso a referência será aquela de uma instância de componente:
*/

/* 
Se o componente filho estiver utilizando a API de Opções ou não 
utilizando <script setup>, a instância referenciada será idêntica
 ao this do componente filho, o que significa que o componente pai 
 terá total acesso as todas propriedades e métodos do componente filho. 
 Isto torna-o fácil de criar detalhes de implementação atrelados 
 firmemente entre o pai e o filho, assim as referências do componente 
 só deve ser utilizadas quando forem absolutamente necessários - na 
 maioria dos casos, deves tentar implementar interações entre o pai e 
 o filho utilizando as interfaces de propriedades e emissão padrão primeiro.
*/

import { ref, onMounted } from "vue";
import Child from "./Child.vue";

const child = ref(null);

onMounted(() => {
  // child.value segurará uma instância de <Child />
});
</script>

<template>
  <Child ref="child" />
</template>

<style lang="css" scoped></style>
