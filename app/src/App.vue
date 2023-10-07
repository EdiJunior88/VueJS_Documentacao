<script setup>
import { computed, h, ref } from "vue";

let id = 0;

const newTodo = ref("");
const hideCompleted = ref(false);
const todos = ref([
  { id: id++, text: "Learn HTML" },
  { id: id++, text: "Learn JavaScript" },
  { id: id++, text: "Learn Vue" },
]);

const filteredTodos = computed(() => {
  // retorna afazeres `todos` filtrados com base nos
  // `todos.value` & `hideCompleted.value`
  return hideCompleted.value ? todos.value.filter((t) => !t.done) : todos.value;
});

function addTodo() {
  todos.value.push({ id: id++, text: newTodo.value });
  newTodo.value = "";
}

function removeTodo(todo) {
  todos.value = todos.value.filter((t) => t !== todo);
}
</script>

<template>
  <form @submit.prevent="addTodo">
    <input v-model="newTodo" />
    <button>Add Todo</button>
  </form>

  <ul>
    <li v-for="todo in filteredTodos" :key="todo.id">
      <input type="checkbox" v-model="todo.done" />
      <span :class="{ done: todo.done }">{{ todo.text }}</span>
      <button @click="removeTodo(todo)">X</button>
    </li>
  </ul>

  <button @click="hideCompleted = !hideCompleted">
    {{ hideCompleted ? "Show all" : "Hide completed" }}
  </button>
</template>

<style lang="css" scoped>
.done {
  text-decoration: line-through;
}
</style>
