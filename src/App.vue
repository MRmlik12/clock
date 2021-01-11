<template>
  <div id="container">
    <div id="mode-changer">
      <mode-changer/>
    </div>
    <div id="clock">
      <Clock/>
    </div>
  </div>
</template>

<script>
import Clock from './components/Clock.vue'
import ModeChanger from './components/ModeChanger.vue'

export default {
  name: 'App',
  components: {
    Clock,
    ModeChanger
  }
}
</script>

<style>
@import url('assets/fontello/css/fontello.css');

@font-face {
  font-family: 'Fontello';
  src: url('assets/fontello/font/fontello.ttf');
}

@font-face {
  font-family: 'OpenSans';
  src: url('assets/open-sans/OpenSans-Bold.ttf')
}

body {
  font-family: 'MyWebFont', 'Fontello', Fallback, sans-serif;
  color: #ffffff;
  background-color: #121212;
}

.container {
  display: inline-block;
}

#mode-changer {
  float: right;
  height: 5%;
}

#clock {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
