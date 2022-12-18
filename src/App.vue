<template>
  <Nav />

  <div class="star-con">
    <span v-for="index in 30" :key=index class="stars dot"></span>

    <span v-for="index in 30" :key=index class="stars star"><svg :width="star_width" :height="star_width / 1.4"
        viewBox="0 0 416 399" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path
          d="M181.275 19.3187C189.644 -6.43958 226.086 -6.43958 234.454 19.3187L264.358 111.352C268.102 122.872 278.835 130.671 290.949 130.671H387.719C414.802 130.671 426.064 165.328 404.153 181.248L325.864 238.127C316.064 245.246 311.963 257.866 315.706 269.385L345.611 361.418C353.979 387.176 324.499 408.598 302.585 392.678L224.299 335.797C214.5 328.679 201.231 328.679 191.431 335.797L113.143 392.678C91.2319 408.598 61.7504 387.176 70.1197 361.418L100.023 269.385C103.766 257.866 99.6656 245.246 89.8667 238.127L11.5785 181.248C-10.333 165.328 0.92808 130.671 28.0119 130.671H124.781C136.894 130.671 147.628 122.872 151.372 111.352L181.275 19.3187Z"
          :fill="star_color" />
      </svg>
    </span>

  </div>

  <!-- <div class="blob"></div>
  <div class="blob"></div> -->

  <router-view />

</template>

<script>
import Nav from '@/components/Nav.vue'

export default {
  components: {
    Nav
  },
  data() {
    return {
      star_color: "white",
      star_width: "10"
    }
  },
  mounted() {
    // function that returns a random number between a min and max
    function getRandomNumber(min, max) {

      return Math.random() * (max - min) + min;

    }
    // collect all the divs
    var divs = document.getElementsByClassName('stars');
    // get window width and height
    var winWidth = window.innerWidth;
    var winHeight = window.innerHeight;
    console.log({ winWidth, winHeight })

    // i stands for "index". you could also call this banana or haircut. it's a variable
    for (var i = 0; i < divs.length; i++) {

      // shortcut! the current div in the list
      var thisDiv = divs[i];

      // get random numbers for each element
      var randomTop = getRandomNumber(0, 100);
      var randomLeft = getRandomNumber(0, 99);

      console.log({ randomTop, randomLeft })

      // update top and left position
      thisDiv.style.top = randomTop + "%";
      thisDiv.style.left = randomLeft + "%";

    }

  }
}

</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400;1,700&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
}

body {
  background-color: black;
  position: relative;
}

#app {
  font-family: 'Space mono', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: black;
  color: white;

  overflow-x: hidden;
}

.stars {
  position: absolute;
}

.dot {
  height: 5px;
  width: 5px;
  background-color: white;
  border-radius: 50%;
  display: inline-block;
}

.blob {
  position: absolute;
  z-index: 0;

  width: 100px;
  height: 500px;
  border-radius: 0 50% 50% 0;

  background-color: rgba(0, 0, 255, 0.397);

  filter: blur(9000px);

}
</style>
