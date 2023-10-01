<script setup>
/* 
Os marcadores de HTML e nomes de atributos são insensíveis a caixa, 
então os navegadores interpretarão quaisquer caracteres maiúsculos 
como minúsculos. Isto significa que quando estiveres utilizando 
modelos de marcação no DOM, nomes de componente em "PascalCase" 
e nomes de propriedades em "camelCase" ou todos os nomes de eventos 
de v-on precisam utilizar os seus equivalentes em "kebab-case" 
(delimitado por hífen):

// "camelCase" em JavaScript
const BlogPost = {
  props: ['postTitle'],
  emits: ['updatePost'],
  template: `
    <h3>{{ postTitle }}</h3>
  `
}

<!-- "kebab-case" em HTML -->
<blog-post post-title="hello!" @update-post="onUpdatePost"></blog-post>
*/
</script>

<template></template>

<style lang="css" scoped></style>
