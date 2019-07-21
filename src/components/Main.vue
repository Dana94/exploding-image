<template>
  <!-- <main>
    <div class="title">
      <h1>Title</h1>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
      <button>Explore</button>
    </div>
    <div>
    </div>
    <section v-for="i in 5" :key="i.id" :class="{dark: i % 2 == 0}">
    </section>
  </main> -->

  <b-container>
    <b-row>
      <b-col cols="6" class="text-left">
        <h1>Title</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
        <button type="button" class="btn btn-warning">Explore</button>
      </b-col>
      <b-col cols="6">Column</b-col>
    </b-row>
    <b-row class="section" v-for="i in 5" :key="i.id" :class="{dark: i % 2 == 0}">
       <b-col cols="12">Column</b-col>
    </b-row>
  </b-container>

</template>

<script>
import Exploder from "./Exploder.vue";
export default {
  components: {
    Exploder
  }
};
</script>

<style lang="scss" scoped>
// main {
//   width: 75%;
//   margin: 0 auto;
//   .title {
//     float: left;
//     display: flex;
//     flex-direction: column;
//     * {
//       display: inline-flex;
//     }
//   }

// section {
//   height: 250px;
//   margin: 0 auto;
//   &.dark {
//     background-color: #ffffff;
//     border-radius: 10px;
//     opacity: 0.25;
//   }
//   @media screen and (max-width: 425px) {
//     // margin-left: 17%;
//   }
// }

.section {
  height: 250px;
  &.dark > div {
    background-color: #ffffff;
    border-radius: 10px;
    opacity: 0.25;
  }
}
</style>
