<template>
  <div class="outer">

    <!-- <div class="img-con"><img class="group" src="../assets/group.jpg" alt=""></div> -->


    <div class="header">

      <h1>We are<br />
        <span class="typed-text">{{ typeValue }}</span>
        <span class="blinking-cursor">|</span>
        <span class="cursor" :class="{ typing: typeStatus }">&nbsp;</span>
      </h1>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',

  props: {
    msg: String
  },

  data() {
    return {
      typeValue: "",
      typeStatus: false,
      displayTextArray: ["Group 6", "HCMUS Spaceship", "US Spaceship", "Ú Spaceship"],
      typingSpeed: 100,
      erasingSpeed: 50,
      newTextDelay: 1000,
      displayTextArrayIndex: 0,
      charIndex: 0,
    }
  },

  created() {
    setTimeout(this.typeText, this.newTextDelay + 200);
  },

  methods: {
    typeText() {
      if (this.charIndex < this.displayTextArray[this.displayTextArrayIndex].length) {
        if (!this.typeStatus) this.typeStatus = true;
        this.typeValue += this.displayTextArray[this.displayTextArrayIndex].charAt(
          this.charIndex
        );
        this.charIndex += 1;
        setTimeout(this.typeText, this.typingSpeed);
      } else {
        this.typeStatus = false;
        setTimeout(this.eraseText, this.newTextDelay);
      }
    },
    eraseText() {
      if (this.charIndex > 0) {
        if (!this.typeStatus) this.typeStatus = true;
        this.typeValue = this.displayTextArray[this.displayTextArrayIndex].substring(
          0,
          this.charIndex - 1
        );
        this.charIndex -= 1;
        setTimeout(this.eraseText, this.erasingSpeed);
      } else {
        this.typeStatus = false;
        this.displayTextArrayIndex += 1;
        if (this.displayTextArrayIndex >= this.displayTextArray.length)
          this.displayTextArrayIndex = 0;
        setTimeout(this.typeText, this.typingSpeed + 1000);
      }
    },
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@500&family=Playfair+Display:ital,wght@0,600;0,653;1,600&display=swap');

.blinking-cursor {
  font-size: 100px;
  color: white;
  -webkit-animation: 1s blink step-end infinite;
  -moz-animation: 1s blink step-end infinite;
  -ms-animation: 1s blink step-end infinite;
  -o-animation: 1s blink step-end infinite;
  animation: 1s blink step-end infinite;
}

@keyframes blink {

  from,
  to {
    color: transparent;
  }

  50% {
    color: red;
  }
}

@-moz-keyframes blink {

  from,
  to {
    color: transparent;
  }

  50% {
    color: red;
  }
}

@-webkit-keyframes blink {

  from,
  to {
    color: transparent;
  }

  50% {
    color: red;
  }
}

@-ms-keyframes blink {

  from,
  to {
    color: transparent;
  }

  50% {
    color: red;
  }
}

@-o-keyframes blink {

  from,
  to {
    color: transparent;
  }

  50% {
    color: red;
  }
}

.header {
  width: 100%;
  max-width: 1400px;
  padding-left: 10px;

  position: relative;
  top: 160px;
  left: 50%;
  transform: translate(-50%);
}


.header h1 {
  width: 100%;
  font-size: 120px;
  line-height: 1em;
  font-style: italic;
  font-weight: 900;

}

h3 {
  margin: 40px 0 0;
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

.logo {
  width: 200px;
  position: absolute;

  top: 0;

}

.outer {
  min-height: 600px;
  width: 100%;

  overflow-x: hidden;
}

img {
  width: 40%;
  max-height: 500px;
  object-fit: cover;

  position: relative;
  left: 50%;
  transform: translate(-50%);

}

.group {
  height: 700px;
}


@media screen and (max-width: 850px) {
  .header {
    height: 200px;
  }

  .header h1 {
    font-size: 60px;
  }

  .blinking-cursor {
    font-size: 60px;
  }
}
</style>
