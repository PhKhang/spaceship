<template>
  <div class="outer">

    <img class="group" src="../assets/group.jpg" alt="">
    <img alt=" logo" class="logo" src="../assets/logodark.png">
    <div class="blur"></div>

    <h1>Welcome to Ú Spaceship</h1>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@500&family=Playfair+Display:ital,wght@0,600;0,653;1,600&display=swap');

h1 {
  width: 900px;
  font-size: 100px;
  position: absolute;
  top: 160px;
  left: 50%;
  transform: translate(-50%);
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
  height: 100vh;
}

img {
  width: 100%;
  object-fit: cover;
  position: relative;
  top: 0;

  left: 0px;
  z-index: 0;
}

.group {
  height: 700px;
}

.blur {
  position: absolute;

  width: 100%;
  height: 800px;

  background: linear-gradient(180deg, rgba(255, 255, 255, 0), black);
  top: 0;
}
</style>
