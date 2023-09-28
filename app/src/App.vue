<script setup>
/* 
Os observadores declarados sincronicamente dentro de setup() 
ou <script setup> estão vinculados a instância do componente 
proprietário, e serão paradas automaticamente quando o 
componente proprietário for desmontado. Na maioria dos casos,
 não precisas te preocupares acerca de parar o observador por ti mesmo.

A chave aqui é que o observador deve ser criado sincronicamente: 
se o observador for criado em uma resposta assíncrona, ele não 
estará vinculado ao componente proprietário e deve ser parado 
manualmente para evitar fugas de memória. Cá está um exemplo:
*/
import { watchEffect } from "vue";

// este aqui será parado automaticamente
watchEffect(() => {});

// ...este aqui não será!
setTimeout(() => {
  watchEffect(() => {});
}, 100);

/* 
Para parar manualmente um observado, utilize a função retornada para 
lidar com isto. Isto funciona para ambos watch e watchEffect:
*/
const unwatch = watchEffect(() => {});

// ...mais tarde, quando for mais necessária
unwatch();

/* 
Nota que deve haver muito poucos casos onde precisas criar observadores 
assincronamente, e criação síncrona deve ser a preferida sempre que possível. 
Se precisares esperar por algum dado assíncrono, podes tornar a tua lógica 
de observação condicional:
*/
// dados a serem carregados assincronamente
const data = ref(null);

watchEffect(() => {
  if (data.value) {
    // faça algo quando os dados forem carregados
  }
});
</script>

<template></template>

<style lang="css" scoped></style>
