<script setup>
import Diary from "./components/Diary.vue";
import Tabs from "./components/Tabs.vue";
import Artilugios from "./components/Artilugios.vue";
import HowTo from "./components/HowTo.vue";
import Concursos from "./components/Concursos.vue";
import Top10 from "./components/Top10.vue";
import Tips from "./components/Tips.vue";
import Historias from "./components/Historias.vue";
import Auth from "./components/Auth.vue";
import { ref } from "vue";
const tabs = ref([
  {
    name: "Diario",
    component: Diary,
  },
  {
    name: "Artilugios Arruinafiestas",
    component: Artilugios,
  },
  {
    name: "Historias de Hazañas",
    component: Historias,
  },
  {
    name: "Tips para Fiestas",
    component: Tips,
  },
  {
    name: "Top 10 ideas para arruinar fiestas",
    component: Top10,
  },
  {
    name: "Recuerdos de Arruinafiestas",
    component: Concursos,
  },
  {
    name: "Como hacer que la gente me quiera",
    component: HowTo,
  },
]);
const solvedAuth = ref(false);
const activeComponent = ref(Diary);
const setActiveComponent = (component) => {
  activeComponent.value = component;
};
const setSolvedAuth = (input) => {
  if (input.password.toLowerCase() === "i did it") {
    solvedAuth.value = true;
  }
};
</script>

<template>
  <div class="page-wrapper">
    <Auth v-if="!solvedAuth" @validInput="setSolvedAuth" />
    <div v-else>
      <div class="tabs">
        <Tabs
          v-for="(tab, index) in tabs"
          :key="`tab-${index}`"
          :tab-name="tab.name"
          :is-active="tab.component === activeComponent"
          :tab-component="tab.component"
          @set-active-component="setActiveComponent"
        />
      </div>
      <div class="page-content">
        <component :is="activeComponent" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.page-wrapper {
  width: 100vw;
  height: 100vh;
}
.tabs {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  width: 100%;
  margin: 0 0 60px 0;
}
.page-content {
  padding: 40px;
}
</style>
