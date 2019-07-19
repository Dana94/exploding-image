<template>
  <main>
    <div class="title">
      <h1>Title</h1>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
      <button>Explore</button>
    </div>
    <div>
      <!-- <exploder></exploder> -->
    </div>
    <section v-for="i in 5" :key="i.id" :class="{dark: i % 2 == 0}">
    </section>
  </main>
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
main {
  width: 75%;
  margin: 0 auto;
  .title {
    float: left;
    display: flex;
    flex-direction: column;
    * {
      display: inline-flex;
    }
    button {
      background-color: #ffcc00;
      border-radius: 10px;
      border-style: none;
      width: 8rem;
      height: 3rem;
      display: inline-block;
    }
  }

  & > div {
    width: 50%;
  }
}

section {
  height: 250px;
  margin: 0 auto;
  &.dark {
    background-color: #ffffff;
    border-radius: 10px;
    opacity: 0.25;
  }
  @media screen and (max-width: 425px) {
    // margin-left: 17%;
  }
}
</style>
