<template>
  <div class="wrapper">
    <svg viewBox="0 0 200.5 112.4">
    <use xlink:href="~/assets/evo-logo.svg#evologo1"/>   
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
  stroke: #000;
  stroke-width: 1;
  stroke-dasharray: 40;
  

  animation: anim 3s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
  animation-timing-function: cubic-bezier(.71,-0.38,.49,1.32);
}
@keyframes anim {
  0% { 
    stroke-dashoffset: 100; 
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
