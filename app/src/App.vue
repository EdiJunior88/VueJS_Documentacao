<script setup>
import { ref, onMounted } from "vue";

// estado reativo
const count = ref(0);

// funções que alteram o estado e acionam atualizações
function increment() {
  count.value++;
}

// gatilhos de ciclo de vida
onMounted(() => {
  console.log(`The initial count is ${count.value}.`);
});
</script>

<template>
  <button @click="increment">Count is: {{ count }}</button>
</template>

<!-- Ambos estilos de API (API de Opções / API de Composição) são completamente capazes de cobrir casos de uso comuns. Eles são interfaces diferentes alimentadas pelo o mesmo exato sistema subjacente. Na verdade, a API de Opções está implementada em cima da API de Composição! Os conceitos fundamentais e conhecimentos a respeito da Vue são partilhas pelos dois estilos.

A API de Opções estão centrados em torno do conceito de um "instância de componente" (this como visto no exemplo), que melhor se alinha normalmente com uma modelo mental de baseado em classe para utilizadores chegando com antecedentes em linguagem de programação orientada a objeto. Isto também é mais amigável a principiantes abstraindo longe os detalhes de reatividade e forçando a organização do código através de grupos de opção.

A API de Composição está centrada em torno da declaração de variáveis de estado reativo imediatamente no escopo de função, e compor estado a partir de várias funções juntas para manipular complexidade. Isto é uma forma mais livre, exige o entendimento de como a reatividade funciona na Vue para ser utilizada eficientemente. Em troca, sua flexibilidade ativam padrões mais poderosos para organização e reutilização de lógica.

Tu podes aprender mais a respeito da comparação entre os dois estilos e os potenciais benefícios da API de Composição na FAQ da API de Composição.

Se fores novo para Vue, cá está nossa recomendação geral:

Para fins de aprendizado, vá com o estilo que parecer-te mais fácil de entender. Novamente, a maioria dos conceitos fundamentais são partilhados entre os dois estilos. Tu podes sempre escolher o outro estilo depois.

Para uso em produção:

Vá com a API de Opções se não estiveres utilizando ferramentas de construção, ou planeias utilizar a Vue primordialmente em cenários de baixa complexidade, por exemplo otimização progressiva.

Vá com a API de Composição + Componentes de Ficheiro Único se planeares construir aplicações completas com a Vue.

Tu não precisas comprometeres-te com apenas um estilo durante a fase de aprendizado. O resto da documentação fornecerá exemplos de código em ambos estilos onde for aplicável, e podes alternar entre eles em qualquer momento utilizando interruptores de Preferência de API no cimo da barra lateral esquerda. -->
