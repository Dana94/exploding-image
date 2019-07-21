<template>
  <!-- <nav>
    <ul>
      <li>Logo</li>
      <li v-for="i in 5" :key="i.id">Link</li>
      <li class="expand">Expand</li>
    </ul>

  </nav> -->
  <div>
    <b-nav>
      <b-nav-item active>Active</b-nav-item>
      <b-nav-item>Link</b-nav-item>
      <b-nav-item>Another Link</b-nav-item>
      <b-nav-item disabled>Disabled</b-nav-item>
    </b-nav>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
  // ul {
  //   display: flex;
  //   justify-content: flex-start;
  //   list-style: none;
  //   padding-left: 0;
  //   li {
  //     margin: 0 20px;
  //     color: #f6f3f1;
  //     &.expand {
  //       position: absolute;
  //       right: 0;
  //     }
  //   }
  // }
  .nav-item a {
    color: #f6f3f1;
  }
</style>
