<template>
  <div id="app">
    <section v-for="i in 5" :key="i.id" :class="{dark: i % 2 == 0}">
      <template v-if="i == 1">
        <div class="exploder">
          <img src="./assets/stairs-books.png" class="books" alt :style="{top: booksTop+'rem'}" />
          <img src="./assets/stairs-ball.png" class="ball" alt :style="{top: ballTop+'rem'}" />
        </div>
      </template>
    </section>
  </div>
</template>

<script>
export default {
  name: "app",
  // https://stackoverflow.com/questions/44804945/vue-js-how-to-react-to-page-scrolling
  data() {
    return {
      scrolled: false,
      booksTop: 22.45,
      ballTop: 0,
      currentY: 0
    };
  },
  methods: {
    handleScroll() {
      // scrolled up

      if (window.scrollY < this.currentY) {
        this.booksTop -= 0.1;
        this.ballTop += 0.1;
      }
      // scrolled up
      else if (window.scrollY > this.currentY) {
        this.booksTop += 0.1;
        this.ballTop -= 0.1;
      }
      this.scrolled = this.currentY > 0;
      console.log(this.scrolled, this.currentY);
      this.currentY = window.scrollY;
    }
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  }
};
</script>

<style lang="scss" scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

section {
  height: 250px;
  &.dark {
    background-color: black;
  }
}
//.exploder {
// position: fixed;
//}
img {
  position: absolute;
  left: 0;
  transition: 0.5s;
}
.books {
  left: 0.5rem;
}
</style>
