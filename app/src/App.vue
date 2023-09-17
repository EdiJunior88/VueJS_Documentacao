<script>
export default {
  // As propriedades retornadas de `data()` tornam-se estados reativos
  // e serão expostas no `this`.
  data() {
    return {
      count: 0,
    };
  },

  // Os métodos são funções que alteram o estado e acionam atualizações.
  // Elas podem ser atadas como ouvintes de evento no modelos de marcação.
  methods: {
    increment() {
      this.count++;
    },
  },

  // Gatilhos do ciclo de vida são chamados em diferentes fases
  // de um ciclo de vida do componente.
  // Esta função será chamada quando o componente for montado.
  mounted() {
    console.log(`The initial count is ${this.count}`);
  },
};
</script>

<template>
  <button @click="increment">Count is: {{ count }}</button>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>
