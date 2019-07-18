<template>
  <nav>
    <ul>
      <li>Logo</li>
      <li v-for="i in 5" :key="i.id">Link</li>
      <li class="expand">Expand</li>
    </ul>

  </nav>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
  ul {
    display: flex;
    justify-content: flex-start;
    list-style: none;
    padding-left: 0;
    li {
      margin: 0 20px;
      &.expand {
        position: absolute;
        right: 0;
      }
    }
  }
</style>
