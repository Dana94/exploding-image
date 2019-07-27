<template>
  <div class="side-bar">
    <template v-for="i in 3">
       <img src="../assets/site-line.svg" alt="" :key="i.id">
        <img src="../assets/site-dot.svg" alt="" :key="i.id" class="dot-img">
    </template>

  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
  .side-bar {
    width: 20px;
    float: left;
    margin: 0 20px;
    display: flex;
    flex-direction: column;
    .dot-img {
      width: 20px;
    }
  }
</style>
