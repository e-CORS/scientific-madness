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
    name: "Caos Acústico",
    image: "/artifacts/caos-sonico.webp",
    desc: " Un dispositivo que distorsiona la música y las voces, creando un caos auditivo en la fiesta. Las canciones se mezclan en tonos discordantes, y las voces de las personas se convierten en sonidos estridentes e incomprensibles.",
  },
  {
    name: "Bomba de pedos",
    image: "artifacts/fart-bomb.webp",
    desc: "Un dispositivo aparentemente inofensivo, pero con un giro inesperado. Emite ruidos de pedos extremadamente realistas y, ocasionalmente, emite un olor similar. Es capaz de imitar toda una sinfonía de flatulencias humanas y animales, desde los sonidos de trompetas hasta los gruñidos de elefantes.",
  },
  {
    name: "Tinta invisible",
    image: "artifacts/invisible-ink.webp",
    desc: " Un compuesto químico que, cuando se rocía en el aire, se adhiere a la ropa de las personas sin que se den cuenta. Luego, al activarlo con calor, las ropas se vuelven fluorescentes o tienen patrones extravagantes, lo que provoca sorpresa y confusión entre los invitados",
  },
  {
    name: "Maquina distorsión musical",
    image: "artifacts/mean-machine.webp",
    desc: "Esta máquina, con apariencia de un viejo gramófono retro, tiene la capacidad de distorsionar cualquier música que reproduzca. Puede ralentizar o acelerar las canciones, invertir los tonos y reproducir los instrumentos al revés. Además, mezcla diferentes géneros musicales en un solo caos sónico, creando una experiencia auditiva surrealista y confusa para los oyentes. El Caos Acústico convierte las melodías en una sinfonía del absurdo.",
  },
  {
    name: "Polvo pica pica",
    image: "artifacts/pica-pica.webp",
    desc: "Este polvo aparentemente inofensivo esconde su verdadero poder. Cuando se dispersa en el aire y entra en contacto con la piel, provoca una sensación de cosquilleo intensa y persistente que resulta incómoda y divertida al mismo tiempo. Además, el polvo cambia de color con cada risa, creando un espectáculo de luces brillantes en la piel de aquellos que caen víctimas del polvo pica pica. Es imposible dejar de reír mientras este polvo juega su travesura.",
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
  height: 120px;
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
  align-items: flex-end;
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
