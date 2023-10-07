<template>
  <div class="tips-wrapper">
    <div
      v-for="(tipsEntry, index) in tips"
      :key="`tip-${index}`"
      class="tips-entry"
    >
      <em class="entry-date">Tip: {{ index + 1 }}</em>
      <br />
      <em class="entry-text">
        {{ tipsEntry.text }}
      </em>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
const tips = ref([
  {
    text: "La fiesta se llevó a cabo en una pequeña sala de estar, donde la iluminación era tenue y las paredes estaban adornadas con un papel pintado anticuado y descolorido. La música de fondo era una melodía monótona que apenas se podía escuchar, y nadie se atrevía a acercarse al reproductor para cambiarla.",
  },
  {
    text: "Los invitados, que parecían haber sido arrastrados a la fiesta por obligación en lugar de entusiasmo, estaban sentados en sofás desgastados y sillas incómodas. Conversaban en susurros, pero sus temas de conversación eran tan insípidos como la decoración: el clima, los informes de tráfico y otros temas igualmente mundanos.",
  },
  {
    text: "La comida consistía en una selección de bocadillos secos y aburridos: galletas saladas, pretzels y una bandeja de zanahorias y apio que nadie tocaba. Las bebidas eran refrescos sin gas que habían perdido su efervescencia hace mucho tiempo.",
  },
  {
    text: "No había actividades ni entretenimiento en la fiesta. No se veían juegos ni concursos, ni siquiera una simple mesa de billar o cartas. La ausencia de cualquier tipo de diversión hacía que el tiempo pasara lentamente.",
  },
  {
    text: "Los anfitriones apenas hacían acto de presencia y, cuando lo hacían, parecían igual de aburridos que sus invitados. No se percibía emoción ni energía en la sala, y las expresiones de todos los presentes reflejaban claramente su deseo de estar en cualquier otro lugar.",
  },
  {
    text: "En resumen, esta fiesta era un ejemplo perfecto de aburrimiento absoluto, donde la falta de ambiente, entretenimiento y conversaciones interesantes la convertía en una experiencia que nadie quería repetir.",
  },
]);
</script>

<style scoped>
.tips-wrapper {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
.tips-entry {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  text-align: left;
  margin-bottom: 50px;
}
</style>
