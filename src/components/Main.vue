<template>
  <b-container>
    <b-row>

          <exploder></exploder>
      
    </b-row>
    <b-row>
      <b-col cols="12" md="6" class="text-left">
        <h1>Title</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
        <button type="button" class="btn btn-warning">Explore</button>
      </b-col>
      <!-- <b-col cols="12" md="6">
        <exploder></exploder>
      </b-col> -->
    </b-row>
    <b-row v-for="i in 3" :key="i.id" class="section">
      <b-col cols="12" md="6" class="content">Image</b-col>
      <b-col cols="12" md="6" class="text content text-left">
        <h1>Title</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
      </b-col>
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
.section {
  height: 250px;
  background-color: #ffffff30;
  border-radius: 10px;
  margin-bottom: 3rem;
  .content {
    background-color: initial;

    h1,
    p {
      color: white;
      background-color: initial;
    }
    &.text {
      padding: 1.5rem;
    }
  }
}
</style>
