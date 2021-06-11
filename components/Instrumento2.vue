<template>
  <div class="folder_container">
    <div class="secondary_info">
      <img src="../assets/img/image2033.png" alt="Perseverance" />
    </div>
    <div class="main_info">
      <h1 class="mission_title">Instrumento: {{ title }}</h1>
      <p class="main_info">{{ main_info }}</p>
      <ul id="v-for-object" class="table_of_contents">
        <li v-bind:key="value.id" v-for="(value, key) in object">
          {{ key }}: {{ value }}
        </li>
      </ul>
    </div>
    <!-- <div class="button_container"><Button /></div> -->
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
      title: "REMS",
      main_info:
        "Estación meteorológica en el rover. Gracias a los instrumentos creados por el CAB para esta misión, tenemos una estación meteorológica en activo en Marte y sabemos la temperatura y la fuerza del viento en tiempo real. Mostramos temperatura y datos en el momento de estar viéndolo.",
      object: {
        Investigador: "Lorem",
      },
    };
  },

  // props: ["title"],
};
</script>

<style lang="scss">
.folder_container2 {
  background-color: rgb(100, 237, 157);
  h1 {
    color: aquamarine;
  }
}
</style>