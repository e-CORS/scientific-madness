<template>
  <div class="diary-wrapper">
    <div
      v-for="(diaryEntry, index) in diary"
      :key="`entry-${index}`"
      class="diary-entry"
    >
      <em class="entry-date">Fecha: {{ diaryEntry.date }}</em>
      <br />
      <em class="entry-text">
        {{ diaryEntry.text }}
      </em>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
const diary = ref([
  {
    date: "2023-7-27",
    text: "Hoy, he ideado el plan perfecto para arruinar la fiesta del señor Thompson. He estado trabajando en una nueva fórmula de tinte que es invisible a simple vista, pero que se revela con el calor. Planeo esconder dispositivos de calor estratégicamente alrededor de la sala, ¡y veré la confusión cuando todos se den cuenta de que están cubiertos de colores brillantes! La risa maliciosa es mi música favorita.",
  },
  {
    date: "2023-4-9",
    text: "Mi última creación, la 'Máquina de Distorsión Musical', ha tenido un gran éxito esta noche. He reprogramado todos los sistemas de sonido de la fiesta para que reproduzcan música clásica a velocidad extrema y al revés. Las caras de horror y desconcierto de los invitados valieron la pena cada hora de trabajo que invertí en ella.",
  },
  {
    date: "2022-11-10",
    text: "Hoy, decidí ser un poco más sutil en mi enfoque. Introduje un compuesto químico en el buffet que hace que todo tenga un sabor extrañamente amargo. Las expresiones de confusión en los rostros de las personas mientras intentan descifrar qué están comiendo son simplemente deliciosas.",
  },
  {
    date: "2022-10-14",
    text: "Mi plan para la próxima fiesta es incluso más ingenioso. Estoy trabajando en un gas inofensivo pero extremadamente fétido que liberaré en la sala. Nadie sospechará nada hasta que sea demasiado tarde. Mi risa retorcida resonará en la habitación mientras todos tratan de escapar del hedor.",
  },
]);
</script>

<style scoped>
.diary-wrapper {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
.diary-entry {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  text-align: left;
  margin-bottom: 50px;
}
</style>
