<script setup>
import { ref } from "vue";
import Home from "./Home.vue";
import Posts from "./Posts.vue";
import Archive from "./Archive.vue";

const currentTab = ref("Home");

const tabs = {
  Home,
  Posts,
  Archive,
};
</script>

<template>
  <div class="demo">
    <button
      v-for="(_, tab) in tabs"
      :key="tab"
      :class="['tab-button', { active: currentTab === tab }]"
      @click="currentTab = tab">
      {{ tab }}
    </button>

    <component :is="tabs[currentTab]" class="tab"></component>
  </div>

  <!-- 
    No exemplo acima, o valor passado para :is pode conter tanto:

    - a sequência de caracteres de nome de um componente registado, OU
    - o objeto de componente importado
    
    Tu também podes utilizar o atributo is para criar elementos de HTML
    regulares.

    Quando estiveres alternando entre vários componentes com <component :is="...">, 
    um componente será desmontado quando ele for alternado para fora. Nós 
    podemos forçar os componentes inativos a manterem-se "vivos" com o componente 
    <KeepAlive> embutido.
   -->
</template>

<style lang="css" scoped>
.demo {
  font-family: sans-serif;
  border: 1px solid #eee;
  border-radius: 2px;
  padding: 20px 30px;
  margin-top: 1em;
  margin-bottom: 40px;
  user-select: none;
  overflow-x: auto;
}

.tab-button {
  padding: 6px 10px;
  border-top-left-radius: 3px;
  border-top-right-radius: 3px;
  border: 1px solid #ccc;
  cursor: pointer;
  background: #f0f0f0;
  margin-bottom: -1px;
  margin-right: -1px;
}

.tab-button:hover {
  background: #e0e0e0;
}

.tab-button:active {
  background: #e0e0e0;
}

.tab {
  border: 1px solid #ccc;
  padding: 10px;
}
</style>
