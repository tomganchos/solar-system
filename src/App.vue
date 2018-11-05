<template>
  <div id="app">
    <p>
      <span id="fog">A long</span>
      <span id="fog-2">long time</span>
      <span id="glow">ago,</span>
      <span id="light">in a</span>
      <span id="stars">galaxy</span>
      <span id="stars-2">far</span>
      <span id="small-stars">far</span>
      <span id="small-stars-2">away&hellip;</span>
    </p>
    <!--<div id="nav">-->
      <!--<router-link to="/">Home</router-link> |-->
      <!--<router-link to="/about">About</router-link>-->
    <!--</div>-->
    <router-view/>

  </div>
</template>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /*text-align: center;*/
  color: #2c3e50;

}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
body {
  background: #000;
  overflow: hidden;
  -webkit-animation-name: pulse;
  -webkit-animation-duration: 30s;
  -webkit-animation-iteration-count: infinite;
  -webkit-animation-timing-function: linear;
}

@-webkit-keyframes pulse {
  from {
    background: #000;
  }
  25% {
    background-color: #003;
  }
  50% {
    background-color: #030;
  }
  to {
    background: #000;
  }
}

p {
  z-index: 0;
  color: rgba(0, 0, 0, 0);
}

#fog,
#fog-2 {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 2000px;
  height: 2000px;
  margin-top: -1000px;
  margin-left: -1000px;
  opacity: .5;
  background: url(./assets/fog.png) repeat-x 0 center;
  -webkit-animation-name: fogAnimation;
  -webkit-animation-duration: 30s;
  -webkit-animation-iteration-count: infinite;
  -webkit-animation-timing-function: linear;
}

#fog-2 {
  opacity: 1;
  -webkit-animation-duration: 120s;
}

@-webkit-keyframes fogAnimation {
  from {
    -webkit-transform: rotate(0deg);
    background-position: 0 center;
  }
  to {
    -webkit-transform: rotate(360deg);
    background-position: 1000px center;
  }
}

#glow {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 800px;
  height: 800px;
  margin: -400px 0 0 -400px;
  background: url(./assets/glow.png) repeat-x 0 0;
  -webkit-animation-name: glowAnimation;
  -webkit-animation-duration: 5s;
  -webkit-animation-iteration-count: infinite;
  -webkit-animation-timing-function: linear;
}

@-webkit-keyframes glowAnimation {
  from {
    opacity: 1;
  }
  50% {
    opacity: .75;
  }
  to {
    opacity: 1;
  }
}

#light {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 800px;
  height: 800px;
  margin: -400px 0 0 -400px;
  background: url(./assets/light.png) no-repeat center center;
  -webkit-animation-name: lightAnimation;
  -webkit-animation-duration: 1s;
  -webkit-animation-iteration-count: infinite;
  -webkit-animation-timing-function: linear;
}

@-webkit-keyframes lightAnimation {
  from {
    opacity: .25;
  }
  50% {
    opacity: .5;
  }
  to {
    opacity: .25;
  }
}

#stars,
#stars-2,
#small-stars,
#small-stars-2 {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 600px;
  height: 600px;
  margin: -300px 0 0 -300px;
  background: url(./assets/stars-large.png) no-repeat center center;
  -webkit-animation-name: starsLarge;
  -webkit-animation-duration: 60s;
  -webkit-animation-iteration-count: infinite;
  -webkit-animation-timing-function: linear;
}

@-webkit-keyframes starsLarge {
  from {
    -webkit-transform: rotate(0deg) scale(3);
    opacity: .1;
  }
  to {
    -webkit-transform: rotate(360deg) scale(.5);
    opacity: 0;
  }
}

#stars-2 {
  -webkit-animation-name: starsLargeAlt;
  -webkit-animation-duration: 45s;
  -webkit-animation-iteration-count: infinite;
  -webkit-animation-timing-function: linear;
}

@-webkit-keyframes starsLargeAlt {
  from {
    -webkit-transform: rotate(180deg) scale(3);
    opacity: .25;
  }
  to {
    -webkit-transform: rotate(360deg) scale(.5);
    opacity: 0;
  }
}

#small-stars,
#small-stars-2 {
  background: url(./assets/stars-small.png) no-repeat center center;
  -webkit-animation-duration: 15s;
  -webkit-animation-name: starsSmall;
}

#small-stars-2 {
  -webkit-animation-name: starsSmallAlt;
  -webkit-animation-duration: 30s;
}

@-webkit-keyframes starsSmall {
  from {
    -webkit-transform: rotate(360deg) scale(3);
    opacity: .25;
  }
  to {
    -webkit-transform: rotate(0deg) scale(.5);
    opacity: 0;
  }
}

@-webkit-keyframes starsSmallAlt {
  from {
    -webkit-transform: rotate(0deg) scale(3);
    opacity: .1;
  }
  to {
    -webkit-transform: rotate(360deg) scale(.5);
    opacity: 0;
  }
}
</style>
