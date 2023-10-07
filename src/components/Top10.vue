<template>
  <div class="topDiez-wrapper">
    <h2>
      Arruinar fiestas siempre es divertido aquí tienes algunas sugerencias para
      que poder lograrlo!
    </h2>
    <ul>
      <li
        v-for="(topDiezEntry, index) in topDiez"
        :key="`topDiezentry-${index}`"
        class="topDiez-entry"
      >
        <h3 v-if="topDiezEntry.title">{{ topDiezEntry.title }}</h3>
        <p class="entry-text">
          {{ topDiezEntry.text }}
        </p>
        <img
          v-if="index === 2"
          src="/star-img.png"
          alt="favorite-star"
          class="favorite"
        />
      </li>
    </ul>

    <p>
      ** Importante recordar tener el antidoto para cuando envenenes la fiesta,
      te recordamos cual es: <strong>H + P + Y + B + Ir + Th + Dy</strong>,
      nunca se sabe cuando por descuido uno pueda comer deliciosa comida
      envenenada, un cientifico precavido sirve para arruinar otra fiesta!!
    </p>
  </div>
</template>

<script setup>
import { ref } from "vue";
const topDiez = ref([
  {
    title: "El Cañón de Confeti Sin Fin:",
    text: "Un enorme cañón que dispara confeti de manera continua y descontrolada, cubriendo a todos los invitados y creando un caos de papel brillante.",
  },
  {
    title: "El Espejo de la Verdad:",
    text: "Un espejo mágico que refleja la verdad sobre las personas que se miran en él. Revela secretos incómodos y verdades inesperadas, causando tensiones y malentendidos entre los invitados.",
  },
  {
    title: "El Envenenamiento",
    text: "Arruinar una noche envenenado la comida de la fiesta siempre es una gran idea para arruinar cualquier fiesta, ha sido probado en varias ocaciones y 60% de las veces funciona el 100% de las veces ***",
  },
  {
    title: "La Bebida Cambiante: ",
    text: "Un brebaje que cambia de sabor y color cada vez que alguien lo toma, creando desconcierto y confusión sobre qué están bebiendo realmente.",
  },
  {
    title: "El Polvo de Baile Hipnótico:",
    text: "Un polvo especial que, cuando se esparce en la pista de baile, hace que todos los invitados bailen de manera extraña y cómica, imitando movimientos ridículos sin poder controlar sus cuerpos.",
  },
  {
    title: "La Silla Musical Acelerada: ",
    text: "Una variante del juego de la silla musical en la que las sillas giran a velocidades aleatorias, haciendo que los participantes caigan y se tambaleen, creando un espectáculo divertido pero desastroso.",
  },
  {
    title: "Los Globos de la Verdad: ",
    text: "Globos llenos de pintura soluble en agua que estallan al contacto, revelando un mensaje de verdad en la ropa de los invitados, exponiendo secretos embarazosos.",
  },
  {
    title: "La Bocina de la Confesión:",
    text: "Una bocina gigante que amplifica cualquier confesión hecha en privado. Las confesiones personales se escuchan en toda la fiesta, creando situaciones incómodas y revelando secretos inesperados.",
  },
  {
    title: "El Espejismo de Invisibilidad: ",
    text: "Un dispositivo que crea la ilusión de que ciertos objetos o personas han desaparecido, creando confusión y desconcierto cuando los invitados intentan encontrar cosas que ya no están allí.",
  },
  {
    title: "El Karaoke Cósmico: ",
    text: "Un sistema de karaoke que modifica las voces de los cantantes, transformándolas en sonidos alienígenas, animales o incluso en voces famosas. Los cantantes se encuentran incapaces de reconocer sus propias voces, creando momentos cómicos.",
  },
  {
    title: "La Lluvia de Mensajes Cómicos:",
    text: "Un proyector que muestra mensajes cómicos y sarcásticos en el techo y las paredes, burlándose de los invitados de manera ingeniosa y creando un ambiente de humor incómodo.",
  },
]);
</script>

<style scoped>
.topDiez-wrapper {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
.topDiez-entry {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;
  text-align: left;
  margin-bottom: 20px;
  position: relative;
  border: 1px solid;
  padding: 10px;
}
.topDiez-entry:nth-child(3) {
  border-color: gold;
}
.favorite {
  position: absolute;
  right: 20px;
  top: 50%;
  width: 40px;
  height: 40px;
}
@media (max-width: 768px) {
  .favorite {
    top: 10px !important;
  }
}
</style>
