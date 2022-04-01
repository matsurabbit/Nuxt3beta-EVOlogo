<script setup lang="ts">
  const cmap = ref({c1:"#01FF6B", c2:"#FF00D0"})
  //const cmap = ref({c1:"#77f277", c2:"#7759bb"})
</script>

<template>
  <div id="parent">
  <div>
    <div id="part1">
      <svg viewBox="0 0 200.5 112.4">
      <linearGradient id="g1" gradientUnits="userSpaceOnUse" gradientTransform="rotate(45)">
        <stop offset="0.5" stop-color="#00000000" stop-opacity="1"/>
        <stop offset="0.5" :stop-color=cmap.c1 stop-opacity="1"/>
      </linearGradient>
      <use xlink:href="~/assets/evo-logo.svg#evologo1"/>
      </svg>
    </div>
    <div id="part2">
      <svg viewBox="0 0 200.5 112.4">
      <linearGradient id="g2" gradientUnits="userSpaceOnUse" gradientTransform="rotate(45)">
        <stop offset="0.5" :stop-color=cmap.c2 stop-opacity="1"/>
        <stop offset="0.5" stop-color="#00000000" stop-opacity="1"/>
      </linearGradient>
      <use xlink:href="~/assets/evo-logo.svg#evologo1"/>
      </svg>
    </div>
  </div>
  </div>
</template>

<style scoped>
#parent {
  background: #000;
  height:200px;
  padding-left: calc((100% - 340px)/2);

}
#parent > div {
  position: relative;
  width: 100px;
  height: 200px;
  padding-left: 100%; /* SVG高さ / SVG幅 * 100 */
  overflow: hidden;
}
#part1, #part2 { 
  position: absolute;
  top: 0;
  left: 0;
  height: 200px;
}
#part1 > svg {
  height: 90%;
  /*margin-top: 25%;*/
  padding: 2%;
  fill: url(#g1);
  filter: drop-shadow(0px 0px 4px v-bind(cmap.c1));
}
#part2 > svg {
  height: 90%;
  /*margin-top: 25%;*/
  padding: 2%;
  fill: url(#g2);
  filter: drop-shadow(0px 0px 5px v-bind(cmap.c2));
}
#part1 {
  animation: anim 4s;
  animation-iteration-count: infinite;
  animation-direction: normal;
  animation-timing-function: cubic-bezier(.38,1.24,.13,1.02);
}
@keyframes anim {
  0% { 
    top: -300px;
    left: 300px;
  }
  30% {
    top: 0px;
    left: -0px;
    /*filter: drop-shadow(0px 0px 3px #096);*/
  }
  100% {
    top: 0px;
    left: -0px;
    /*filter: drop-shadow(0px 0px 3px #096);*/
  }
}
</style>
