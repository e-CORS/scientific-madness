<template>
  <div
    v-for="(artilugio, index) in artilugios"
    :key="`artilugio-${index}`"
    class="artilugio-wrapper"
  >
    <img :src="artilugio.image" alt="artilugio-image" class="artilugio-image" />
    <div class="artilugio-text">
      <h3>{{ artilugio.name }}</h3>
      <p class="artilugio-desc">
        {{ artilugio.desc }}
      </p>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
const artilugios = ref([
  {
    name: "Fiesta de graduacion del 95'",
    image: "concursos/fiesta-arruinada-2.jpg",
    desc: "Como olvidar el dia que Carl Steffen arruino la graduacion de tanta gente, un maestro en el arte! merecido ganador de 'Arruinador ACME del año'",
  },
  {
    name: "Juntada Epica",
    image: "concursos/juntada.jpg",
    desc: "Que juntada tremenda, un dia de importantes intercambios y donde conoci a mi gran secuaz nico! un tipo con mucho potencial para el caos!!",
  },
  {
    name: "Celebrando el cumpleaños del unico e inolvidable Kim bole el maestro del aburrimiento!!",
    image: "concursos/fiesta-arruinada-3.jpg",
    desc: "Tremendo los muchachos como chupaban whisky!!",
  },
]);
</script>

<style scoped>
.artilugio-wrapper {
  display: flex;
  flex-grow: 1;
  border: 1px solid;
  padding: 10px;
  margin-bottom: 10px;
}
.artilugio-image {
  margin-right: 50px;
}
.artilugio-text {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  text-align: left;
}
.artilugio-desc {
  text-align: left;
}
.artilugio-wrapper:nth-child(even) {
  display: flex;
  flex-direction: row-reverse;
}
.artilugio-wrapper:nth-child(even) > .artilugio-text {
  margin-right: 50px;
}
.artilugio-wrapper:nth-child(even) > .artilugio-image {
  margin-right: unset;
}

@media (max-width: 600px) {
  .artilugio-wrapper {
    flex-direction: column !important;
    align-items: center !important;
  }
  .artilugio-image {
    margin: unset !important;
  }
}
</style>
