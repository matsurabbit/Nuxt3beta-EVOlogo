<template>
  <div class="wrapper">
    <svg viewBox="0 0 2152.07 1291.96">
    <use xlink:href="~/assets/evo-logo-just.svg#evologo2"/>   
    </svg>
  </div>
</template>

<style scoped>
.wrapper {
  position: relative;
  height: 100%;
}
.wrapper svg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
svg {
  fill: #42AFE3;
  stroke: #55009977;
  stroke-width: 25;
  stroke-dasharray: 500;
  stroke-linecap: round;
  stroke-linejoin: round;
  paint-order: stroke;

  animation: anim 3s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  animation-timing-function: cubic-bezier(.71,-0.38,.49,1.32);
}
@keyframes anim {
  0% { 
    stroke-dashoffset: 1500; 
    fill: #ab4567;
  }
  50% { 
    fill: #fff;
  }
  100% {
    stroke-dashoffset: 0;
    fill: #02468a;
  }
}
</style>
