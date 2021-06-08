<template>
  <div class="folder_container ">
    <div class="secondary_info">
      <img src="../assets/img/perseverance.png" alt="Curiosity" />
    </div>
    <div class="main_info">
      <h1 class="mission_title">Misión: {{ title }}</h1>
      <p class="main_info">{{ main_info }}</p>
      <ul id="v-for-object" class="table_of_contents">
        <li v-bind:key="value.id" v-for="(value, key) in object">
          {{ key }}: {{ value }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import Button from "../components/Button";

export default {
  components: {
    Button,
  },

  data() {
    return {
      title: "Curiosity",
      main_info:
        "La Mars Science Laboratory (abreviada MSL), conocida como Curiosity, es una misión espacial que incluye un rover de exploración marciana dirigida por la NASA. La duración prevista de la misión era de 1 año marciano (1,88 años terrestres), aunque en junio de 2020 aún sigue operativa. El control del rover se realiza desde la tierra y su velocidad es de 130 metros a la hora.",
      object: {
        Nacionalidad: "Lorem",
        Agencia: "Lorem",
        Lanzamiento: "Lorem",
        Llegada: "Lorem",
        Lugar: "Lorem",
      },
    };
  },

  // props: ["title"],
};
// Vue.component('titulo-mision',{
//     props: ['title'],
//     template: <h2>{{title}}</h2>
// }
// )
</script>

<style lang="scss">
.folder_container {
  color: white;
  .main_info {
  }
  .secondary_info {
  }
}
</style>