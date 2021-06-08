<template>
    <div class="scoll_menu">
        
<!-- <h1 v-bind:is="title"></h1>         -->
<!-- <titulo-mision title="Curiosity"> </titulo-mision> -->
                <h2 id="menu1" class="scrollMenuItem">Curiosity</h2>
                <h3 id="menu2" class="scrollMenuItem">Instrumento</h3>
                <h3 id="menu3" class="scrollMenuItem">Objetivos</h3>

    </div>
</template>
<script>



import Folder from "../components/Folder";


export default {

  components: { Folder },


    mounted() {
        
    },
}
</script>

<style lang="scss">

</style>