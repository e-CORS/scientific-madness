<template>
  <div class="history-wrapper">
    <div
      v-for="(historyEntry, index) in history"
      :key="`history-${index}`"
      class="history-entry"
    >
      <h3 class="entry-title">{{ historyEntry.title }}</h3>
      <br />
      <em class="entry-text">
        {{ historyEntry.text }}
      </em>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const history = ref([
  {
    title: "El Baile Incontrolable:",
    text: "Libere una lluvia constante de confeti en un evento al aire libre, creando un caos de papel brillante que cubría todo y dejaba a las personas asombradas y divertidas, pero también completamente cubiertas de confeti.",
  },
  {
    title: "El Día de la Lluvia de Confeti:",
    text: "Mi última creación, la 'Máquina de Distorsión Musical', ha tenido un gran éxito esta noche. He reprogramado todos los sistemas de sonido de la fiesta para que reproduzcan música clásica a velocidad extrema y al revés. Las caras de horror y desconcierto de los invitados valieron la pena cada hora de trabajo que invertí en ella.",
  },
  {
    title: "La Conferencia de Risas:",
    text: "Interrumpi una conferencia científica seria con su gas de la risotada, haciendo que los asistentes, incluidos los científicos más respetados, no pudieran dejar de reírse durante horas. La conferencia se convirtió en una hilarante reunión que fue imposible de tomar en serio.",
  },
  {
    title: "La Fiesta del Espejismo:",
    text: "Organice una fiesta en un lugar que solo existía como un holograma, haciendo que los invitados se encontraran bailando en un lugar que, en realidad, no estaba ahí. Esta experiencia surrealista dejó a todos preguntándose si habían estado en la fiesta en primer lugar.",
  },
  {
    title: "La Carrera de Confusión::",
    text: "Organice una carrera de obstáculos en la que los obstáculos eran ilusiones ópticas creadas por su proyector de hologramas. Los participantes se encontraron corriendo hacia paredes que no existían y saltando obstáculos que desaparecían, creando una escena de total desconcierto y diversión.",
  },
  {
    title: "El Desfile de Sombras:",
    text: "Organice un desfile de sombras gigantes en la noche, proyectando siluetas enormes y extrañas en los edificios de la ciudad. Esto creó una atmósfera surrealista y fantasmagórica que dejó a la ciudad entera preguntándose si estaban experimentando un evento sobrenatural.",
  },
]);
</script>

<style scoped>
.history-wrapper {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
.history-entry {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  text-align: left;
  margin-bottom: 50px;
}
</style>
