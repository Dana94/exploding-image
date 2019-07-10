<template>
  <div id="app">
    <section v-for="i in 10" :key="i.id" :class="{dark: i % 2 == 0}">
      <template v-if="i == 1">
        <div class="exploder">
          <img src="./assets/larger-books.png" class="books" alt :style="{top: booksTop+'px'}" />
          <img src="./assets/larger-ball.png" class="ball" alt :style="{top: ballTop+'px'}" />
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
      booksTop: 0,
      ballTop: 0,
      currentY: 0
    };
  },
  methods: {
    handleScroll() {
      // back top top
      if(window.scrollY == 0){
        console.log("back to top: ", window.scrollY);
        this.booksTop = 0;
        this.ballTop = 0;
      }
      // scrolled up
      else if (this.currentY > 0 && window.scrollY < this.currentY){// && window.scrollY % 10 == 0) {
        console.log("up: ", window.scrollY);
        this.booksTop -= 4.53386;
        this.ballTop -= .755645;
      }
      // scrolled down
      else if (this.currentY > 0 && window.scrollY > this.currentY){// && window.scrollY % 10 == 0) {
        console.log("down: ", window.scrollY);
        this.booksTop += 4.53386;
        this.ballTop += .755645;
      }
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
  // position: absolute;
  // left: 0;
  // transition: 0.5s;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 50%;
  -webkit-transform: translateX(-50%);
  transform: translateX(-50%);
  max-height: 100%;
  max-width: 100%;
  transition: 0.5s;
}
</style>
