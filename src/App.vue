<template>
  <center>
    <img alt="Vue logo" src="./assets/logo.png" width="50" /><br />
  </center>
  <hr />
  <center><h1>Vue 3 Exercise</h1></center>
  <div v-bind:class="classCard" v-for="(component, i) in arrList" :key="i">
    <component v-bind:is="component"></component>
  </div>
  <Footer class="classFooter" msg="Footer for Your Vue.js App" />
</template>

<script>
import Exercise01 from "./components/Vue01_data";
import Exercise02 from "./components/Vue02_declaritive_rendering";
import Exercise03 from "./components/Vue03_vbind";
import Exercise04 from "./components/Vue04_vonce";
import Exercise05 from "./components/Vue05_vshow";
import Exercise06 from "./components/Vue06_vif";
import Exercise07 from "./components/Vue07_vfor";
import Exercise08 from "./components/Vue08_von";
import Exercise09 from "./components/Vue09_von_Event";
import Exercise10 from "./components/Vue10_von_keyEvent";
import Exercise11 from "./components/Vue11_von_mouseEvent";
import Exercise12 from "./components/Vue12_von_capture_self";
import Exercise13 from "./components/Vue13_checkbox";
import Exercise14 from "./components/Vue14_radio";
import Exercise15 from "./components/Vue15_select";
import Exercise16 from "./components/Vue16_checkbox_binding";
import Exercise17 from "./components/Vue17_radio_binding";
import Exercise18 from "./components/Vue18_select_binding_o";
import Exercise19 from "./components/Vue19_select_binding_c";
import Exercise20 from "./components/Vue20_form_element_join";
import Exercise21 from "./components/Vue21_o_c_ref_reactive";
import Exercise22 from "./components/Vue22_scriptsetup";
import Exercise23 from "./components/Vue23_vpre";
import Exercise24 from "./components/Vue24_computed";
import Exercise25 from "./components/Vue25_watcheffect";
import Footer from "./components/Vue_Footer";
export default {
  name: "App",
  components: {
    Exercise01,
    Exercise02,
    Exercise03,
    Exercise04,
    Exercise05,
    Exercise06,
    Exercise07,
    Exercise08,
    Exercise09,
    Exercise10,
    Exercise11,
    Exercise12,
    Exercise13,
    Exercise14,
    Exercise15,
    Exercise16,
    Exercise17,
    Exercise18,
    Exercise19,
    Exercise20,
    Exercise21,
    Exercise22,
    Exercise23,
    Exercise24,
    Exercise25,

    Footer,
  },
  data() {
    return {
      arrList: [
        Exercise01,
        Exercise02,
        Exercise03,
        Exercise04,
        Exercise05,
        Exercise06,
        Exercise07,
        Exercise08,
        Exercise09,
        Exercise10,
        Exercise11,
        Exercise12,
        Exercise13,
        Exercise14,
        Exercise15,
        Exercise16,
        Exercise17,
        Exercise18,
        Exercise19,
        Exercise20,
        Exercise21,
        Exercise22,
        Exercise23,
        Exercise24,
        Exercise25,

      ],
      classCard: "card",
      classFooter: "footer",
    };
  },
};
</script>

<style>
body {
  display: flex;
  align-items: center;
  flex-direction: column;
  background-color: rgba(231, 243, 243, 0.829);
  padding: 20px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

/* #app > div {
    padding: 10px;
    margin-bottom: 55px;
    background-color: white;
    border-radius: 5px;
    box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
    transition: 0.3s all ease-in-out;
  } */

#app > div:focus,
#app > div:hover {
  box-shadow: rgba(0, 0, 0, 0.7) 0px 4px 12px;
}

#app > div > h1 {
  text-align: center;
}

.card {
  width: 500px;
  padding: 10px;
  margin-bottom: 55px;
  background-color: white;
  border: 1px solid rgba(0, 0, 0, 0.192);
  border-radius: 20px;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
  transition: 0.3s all ease-in-out;
}
.footer {
  height: 200px;
  margin: 0;
  background-color: gray;
  line-height: 90px;
  padding-left: 50px;
  font-weight: bold;
  text-align: center;
  clear: both;
}
</style>