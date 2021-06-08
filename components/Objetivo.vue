<template>
  <div class="folder_container">
    
    <ul id="v-for-object" class="objetivos_table_of_contents">
        <li v-bind:key="value.id" v-for="value in object">
         {{ value }}
        </li>
      </ul>
        <div class="button_container"><Button /></div>

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
           object: {
        objetivo1: "Determinar si existió vida alguna vez en Marte.",
        objetivo2: "Caracterizar el clima de Marte.",
        objetivo3: "Determinar su geología.",
        objetivo4: "Prepararse para la exploración humana de Marte.",
      },
    };
  },

};

</script>


<style lang="scss">

</style>