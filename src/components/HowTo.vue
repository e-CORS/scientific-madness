<template>
  <div class="howto-wrapper">
    <h2>
      Fomentar el afecto y la amistad de las personas es un proceso que se basa
      en la empatía, el respeto y la autenticidad.
    </h2>
    <h3>
      Aquí tienes algunas sugerencias para que las personas te quieran y te
      aprecien:
    </h3>
    <ul>
      <li
        v-for="(howtoEntry, index) in howto"
        :key="`tip-${index}`"
        class="howto-entry"
      >
        <h5 v-if="howtoEntry.title">{{ howtoEntry.title }}</h5>
        <p class="entry-text">
          {{ howtoEntry.text }}
        </p>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from "vue";
const howto = ref([
  {
    title: "Sé tú mismo:",
    text: "La autenticidad es fundamental. No trates de ser alguien que no eres para agradar a los demás. La gente valora la sinceridad.",
  },
  {
    title: "Escucha activamente: ",
    text: "Presta atención a lo que dicen los demás, muestra interés genuino por sus pensamientos y sentimientos. Haz preguntas y muestra empatía hacia sus experiencias.",
  },
  {
    title: "Sé amable y respetuoso: ",
    text: "Trata a los demás con cortesía y consideración. Pequeños actos de amabilidad pueden marcar una gran diferencia.",
  },
  {
    title: "Ofrece apoyo:",
    text: " Está ahí para tus amigos y seres queridos cuando lo necesiten. Escuchar, ofrecer ayuda y mostrar comprensión son formas efectivas de construir relaciones sólidas.",
  },
  {
    title: "Comparte tus experiencias:",
    text: " Comparte tus pensamientos, intereses y pasiones. Compartir experiencias similares puede fortalecer los lazos entre las personas.",
  },
  {
    title: "Muestra gratitud: ",
    text: "Agradece a las personas por su amistad y apoyo. Reconocer lo que hacen por ti fortalece los lazos emocionales.",
  },
  {
    title: "Sé confiable: ",
    text: "Cumple tus promesas y mantén la confidencialidad cuando sea necesario. La confianza es esencial en cualquier relación.",
  },
  {
    title: "Desarrolla habilidades de comunicación: ",
    text: "Aprende a comunicarte de manera efectiva, tanto verbalmente como a través del lenguaje corporal. La comunicación clara ayuda a evitar malentendidos y conflictos.",
  },
  {
    title: "Sé paciente: ",
    text: "Construir relaciones significativas lleva tiempo. No esperes que la gente te quiera de inmediato. La paciencia es clave.",
  },
  {
    title: "Aprende a perdonar: ",
    text: "Las personas cometen errores. Si alguien te lastima, considera perdonar y darles una segunda oportunidad si sientes que lo merecen.",
  },
  {
    text: "Recuerda que no todas las personas responderán de la misma manera, y es posible que algunas no te quieran, a pesar de tus mejores esfuerzos. Lo importante es ser auténtico y buscar relaciones saludables y mutuamente beneficiosas.",
  },
]);
</script>

<style scoped>
.howto-wrapper {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
.howto-entry {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  text-align: left;
  margin-bottom: 20px;
}
</style>
