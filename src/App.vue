<template>
  <div id="app">
    <app-nav></app-nav>
    <side-bar></side-bar>
    <app-main></app-main>
  </div>
</template>

<script>
import Nav from './components/Nav.vue';
import SideBar from './components/SideBar.vue';
import Exploder from './components/Exploder.vue';
import Main from './components/Main.vue';


export default {
  name: "app",
  // https://stackoverflow.com/questions/44804945/vue-js-how-to-react-to-page-scrolling
  data() {
    return {

    };
  },
  components: {
    appNav: Nav,
    SideBar,
    Exploder,
    appMain: Main
  }
};
</script>

<style lang="scss">
@import './assets/base.scss';
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #cad0d6;
  margin-top: 60px;
}




</style>
