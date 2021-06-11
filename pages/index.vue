<template>
  <div>
    <!-- <Logo /> -->
    <div class="container0">
      <div class="background_image">
        <img src="../assets/img/JEZERO_091.png" alt="" />
      </div>
      <div class="black_bcground">
                <div class="button_container"><Button /></div>

      </div>
      <div id="endcontainer" class="spacer s0"></div>

      <div id="pinContainer" class="spacer s0"></div>

      <div id="animate0">
<div class="scoll_menu">
   
    <h2 id="menu1" class="scrollMenuItem">Curiosity</h2>
    <h3 id="menu2" class="scrollMenuItem">Instrumento</h3>
    <h3 id="menu3" class="scrollMenuItem">Objetivos</h3>

    <div class="other-tabs">
      <h2 class="scrollMenuItem"> 
        <NuxtLink class="nuxtlink" to="/pagina2">Perseverance</NuxtLink>
        </h2>
      <h2 class="scrollMenuItem">Insight</h2>
    </div>
  </div>
        <div class="container1">
          <div id="animate1 ">
            <Folder />
          </div>
        </div>
        <div id="endContainer1" class="spacer s0"></div>

        <div id="pinContainer2" class="spacer s0"></div>

        <div class="container2">
          <div id="animate2">
            <Instrumento />
          </div>
        </div>
        <div id="endContainer2" class="spacer s0"></div>

        <div id="pinContainer3" class="spacer s0"></div>

        <div class="container3">
          <div id="animate3">
            <Objetivo />
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
import Logo from "../components/Logo";
import Button from "../components/Button";
import Folder from "../components/Folder";
import ScrollMenu from "../components/ScrollMenu";
import Instrumento from "../components/Instrumento";
import Objetivo from "../components/Objetivo";

export default {
  components: {
    Logo,
    Button,
    Folder,
    Instrumento,
    Objetivo,
    ScrollMenu,
    Button,
  },

  mounted() {
    const controller = new this.$scrollmagic.Controller();

    var scene0 = new this.$scrollmagic.Scene({
      triggerElement: ".container1",
      triggerHook: 0.3,
      duration: "80%",
      offset: 70,
    })

      .setPin(".container1")
      .setClassToggle("#menu1", "active_menu")
      .addIndicators() //

      .addTo(controller);

    var porfifunciona = new this.$scrollmagic.Scene({
      triggerElement: ".container1",
      triggerHook: 0.3, //show, then scroll 10% into  view
      duration: "80%", //hide 10% before exiting view
      offset: 70,
    })
      .setClassToggle(".container1", "visible") // add class to reveal
      .addIndicators() // add indicators (requires plugin)

      .addTo(controller);

    var scene1 = new this.$scrollmagic.Scene({
      triggerElement: "#pinContainer2",
      triggerHook: 0.3, //show, then scroll 10% into  view
      duration: "80%", //hide 10% before exiting view
      offset: 20, //movetiggertocenter of element
    })
      // .setTween(".container2", 5, { opacity: "0" })
      .setPin(".container2")

      .setClassToggle("#menu2", "active_menu")

      .addIndicators() // add indicators (requires plugin)

      .addTo(controller);

    var porfifunciona2 = new this.$scrollmagic.Scene({
      triggerElement: ".container2",
      triggerHook: 0.3, //show, then scroll 10% into  view
      duration: "70%", //hide 10% before exiting view
      offset: 20,
    })
      .setClassToggle(".container2", "visible") // add class to reveal
      .addIndicators() // add indicators (requires plugin)

      .addTo(controller);

    var scene2 = new this.$scrollmagic.Scene({
      triggerElement: "#pinContainer3",
      triggerHook: 0.3, //show, then scroll 10% into  view
      duration: "70%", //hide 10% before exiting view
      offset: 20, //movetiggertocenter of element
    })
      // .setTween(".container3", 5, { opacity: "0" })
      .setPin(".container3")
      .setClassToggle(".container3", "visible") // add class to reveal

      .setClassToggle("#menu3", "active_menu")

      .addIndicators() // add indicators (requires plugin)

      .addTo(controller);

    var porfifunciona3 = new this.$scrollmagic.Scene({
      triggerElement: ".container3",
      triggerHook: 0.3, //show, then scroll 10% into  view
      duration: "80%", //hide 10% before exiting view
      offset: 20,
    })
      .setClassToggle(".container3", "visible") // add class to reveal

      .addTo(controller);
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Alegreya:ital,wght@0,400;0,500;0,600;0,700;0,800;0,900;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Alegreya+Sans:ital,wght@0,100;0,300;0,400;0,500;0,700;0,800;0,900;1,100;1,300;1,400;1,500;1,700;1,800;1,900&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Alegreya+Sans+SC:ital,wght@0,100;0,300;0,400;0,500;0,700;0,800;0,900;1,100;1,300;1,400;1,500;1,700;1,800;1,900&family=Alegreya+Sans:ital,wght@0,100;0,300;0,400;0,500;0,700;0,800;0,900;1,100;1,300;1,400;1,500;1,700;1,800;1,900&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Alegreya+SC:ital,wght@0,400;0,500;0,700;0,800;0,900;1,400;1,500;1,700;1,800;1,900&family=Alegreya+Sans+SC:ital,wght@0,100;0,300;0,400;0,500;0,700;0,800;0,900;1,100;1,300;1,400;1,500;1,700;1,800;1,900&family=Alegreya+Sans:ital,wght@0,100;0,300;0,400;0,500;0,700;0,800;0,900;1,100;1,300;1,400;1,500;1,700;1,800;1,900&display=swap");

.background_image {
  // overflow: hidden;
  position: fixed;
  img {
    width: 110vw;
    height: 100vh;
    object-fit: cover;
    background-repeat: no-repeat;
    filter: saturate(20%);
  }
}
.spacer {
  height: 0;
}
// #pinContainer {
//   width: 100%;
//   height: 100%;
//   overflow: hidden;
//   -webkit-perspective: 1000;
//   perspective: 1000;
// }

// .zap {
//   transform: scale(2.5, 0);
// }

// #animate2 {
//   transition: transform 0.3s ease-out;
// }
// #animate1 {
//   transition: transform 0.3s ease-out;
// }
.nuxtlink{
text-decoration: none;
font-weight: inherit;
font-family: inherit;
color: inherit;}

.container {
  margin: 0 auto;
  min-height: 10vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.container1 {
}
.container2 {
  // margin: 0 auto;
  // // min-height: 100vh;
  // // display: flex;
  // // justify-content: center;
  // // align-items: center;
  // // text-align: center;
}

// .container3 {
//   margin: 0 auto;
//   min-height: 100vh;
//   display: flex;
//   justify-content: center;
//   align-items: center;
//   text-align: center;
// }

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
