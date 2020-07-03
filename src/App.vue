<template>
  <div id="app">
    <game-header></game-header>
    <game-footer></game-footer>
    <game-main></game-main>
  </div>
</template>

<script>
import GameHeader from "./components/GameHeader";
import GameFooter from "./components/GameFooter";
import GameMain from "./components/GameMain";

export default {
  components: {
    "game-header": GameHeader,
    "game-footer": GameFooter,
    "game-main": GameMain
  }
};

/*
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld
  }
};
*/
</script>

<style>
html,
body {
  background-color: #a29bfe;
  font-family: Arial, Helvetica, sans-serif;
  margin: 0;
  padding: 0;
}

.wrapper {
  margin: 0 auto;
  width: 80%;
  border: 0px solid red;
}

.cards_container {
  margin: 0 auto;
  border: 0px solid white;
  align-content: center;
  text-align: center;
}

.card {
  width: 200px;
  height: 200px;
  background-color: #6c5ce7;
  border-radius: 10px;
  display: inline-block;
  margin: 10px 20px 10px 20px;
  box-shadow: 0 2px 6px 0 rgba(0, 0, 0, 0.2), 0 4px 24px 0 rgba(0, 0, 0, 0.19);
  transform: scale(1);
  animation: pulse 5s infinite;
}

@keyframes pulse {
  0% {
    transform: scale(0.95);
  }

  70% {
    transform: scale(1);
  }

  100% {
    transform: scale(0.95);
  }
}

/*
.flip-card{
    width:200px;
    height:200px;
    background-color: #6c5ce7;
    border-radius:10px;
    display:inline-block;
    margin: 10px 20px 10px 20px;
    box-shadow: 0 2px 6px 0 rgba(0, 0, 0, 0.2), 0 4px 24px 0 rgba(0, 0, 0, 0.19);
    transform: scale(1);
    animation: pulse 5s infinite;
    perspective: 1000;
    min-height: 120px;
    cursor: pointer;
}


.front-card,
.back-card {

    backface-visibility: hidden;
    transition: 0.6s;
    transform-style: preserve-3d;
    top: 0;
    left: 0;
    width: 100%;
}
.back-card {
    transform: rotateY(-180deg);
    position: absolute;
    background-color: #FFFFFF;
}

*/

.flip_card {
  width: 210px;
  height: 200px;
  background-color: #6c5ce7;
  border-radius: 10px;
  display: inline-block;
  margin: 10px 20px 10px 20px;
  box-shadow: 0 2px 6px 0 rgba(0, 0, 0, 0.2), 0 4px 24px 0 rgba(0, 0, 0, 0.19);
  transform: scale(1);
  animation: pulse 5s infinite;
  perspective: 1000;
  min-height: 120px;
  cursor: pointer;
}

/* This container is needed to position the front and back side */
.flip_card_inside {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

/* Do an horizontal flip when you move the mouse over the flip box container */
.flip_card:hover .flip_card_inside {
  transform: rotateY(180deg);
}

/* Position the front and back side */
.flip_card_front,
.flip_card_back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
}

.flip_card_back {
  background-color: #ffffff;
  color: #000000;
  transform: rotateY(180deg);
  border-radius: 10px;
}

.card_flip_image {
  padding-top: 40px;
}

/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}*/
</style>
