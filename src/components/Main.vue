<template>
  <main>
    <div class="title">
      <h1>Title</h1>
      <p>Text...</p>
      <button>Explore</button>
    </div>
    <div>
      <exploder></exploder>
    </div>
  </main>
</template>

<script>
import Exploder from './Exploder.vue';
export default {
  components: {
    Exploder
  }

}
</script>

<style lang="scss" scoped>
main {
  width: 75%;
  margin: 0 auto;
  .title {
    float: left;
  }
}
</style>
