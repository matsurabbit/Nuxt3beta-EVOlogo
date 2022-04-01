<template>
  <div class="wrapper">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 2152.07 1291.96">
      <use xlink:href="~/assets/evo-logo-just.svg#evologo2"/>   
    </svg>
  </div>
</template>

<style scoped>
.wrapper {
  position: relative;
  height: 100%;
  padding-left: 100%; /* SVG高さ / SVG幅 * 100 */
}
.wrapper svg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
svg {
  fill: #000;
  stroke: #000;
  stroke-width: 5;
  stroke-opacity: 0.5;
  stroke-linecap: round;

  animation: anim 2s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  animation-timing-function: cubic-beziercubic-bezier(.48,-0.1,0,1.06);
}
@keyframes anim {
  0% { 
    stroke-width: 0;
    stroke-opacity: 0;
  }
  100% {
    stroke-width: 5px;
    stroke-opacity: 0.5;
    filter: drop-shadow(0px 0px 4px #096);
  }
}
</style>
