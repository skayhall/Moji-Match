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
</style>
