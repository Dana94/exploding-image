<template>
  <div class="exploder">
    <img src="../assets/platform-1.png" class="image-1" alt :style="{top: image1+'px'}" />
    <img src="../assets/stairs-2.png" class="image-2" alt :style="{top: image2+'px'}" />
    <img src="../assets/stairs-3.png" class="image-3" alt :style="{top: image3+'px'}" />
    <img src="../assets/platform-4.png" class="image-4" alt :style="{top: image4+'px'}" />
    <img src="../assets/chair-5.png" class="image-5" alt :style="{top: image5+'px'}" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      image1: 0,
      image2: 0,
      image3: 0,
      image4: 0,
      image5: 0,
      currentY: 0
    };
  },
  methods: {
    handleScroll() {
      // back top top
      console.log("height", window.innerHeight);
      if (window.scrollY == 0) {
        console.log("back to top: ", window.scrollY);
        this.image1 = 0;
        this.image2 = 0;
        this.image3 = 0;
        this.image4 = 0;
        this.image5 = 0;
      }
      // scrolled up
      else if (this.currentY > 0 && window.scrollY < this.currentY) {
        this.image1 -= 3.6;
        this.image2 -= 0.6;
        this.image3 -= -2.4;
        this.image4 -= -5.4;
        this.image5 -= -8.4;
      }
      // scrolled down
      else if (this.currentY > 0 && window.scrollY > this.currentY) {
        this.image1 += 3.6;
        this.image2 += 0.6;
        this.image3 += -2.4;
        this.image4 += -5.4;
        this.image5 += -8.4;
        // }
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

  &.image-3 {
    z-index: 1;
  }
}
</style>
